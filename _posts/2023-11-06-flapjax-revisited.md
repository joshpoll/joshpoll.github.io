---
title: "Flapjax Revisited"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

Reactive programming for UI applications has been studied for a long time. But while the academic
literature has focused mostly on functional reactive programming (FRP), which uses behaviors and events, the web has adopted a different
approach: signals.

Why did signals win? Is this a case of worse-is-better or is there something deeper going on? I
think there are some good reasons why signals won. In this post we'll compare and contrast Flapjax, a JS FRP
library, and Solid's signals.

<!--more-->

**Note:** This post assumes you are familiar with Solid's signal system.
{: .notice}

# Flapjax Revisited

In 2009, Meyerovich et al. published "Flapjax: A Programming Language for Ajax
Applications," which argued for functional reactive programming for the web. But now, nearly 15
years later, functional reactive programming seems to have lost to signals. Why?

Let's start by looking at the motivating example from the Flapjax paper:

```js
var timerID = null;
var elapsedTime = 0;

function doEverySecond() {
  elapsedTime += 1;
  document.getElementById("curTime").innerHTML = elapsedTime;
}

function startTimer() {
  timerId = setInterval("doEverySecond()", 1000);
}

function resetElapsed() {
  elapsedTime = 0;
  // bug! The DOM is not updated until the next call to doEverySecond
}

<body onload="startTimer()">
  <input id="reset" type="button" value="Reset" onclick="resetElapsed()" /> <div id="curTime"> </div>
</body>;
```

This is the thought process the authors claim a developer must go through when reading this code:

1. The value is ostensibly displayed by the second line of the function `doEverySecond`.
2. The value displayed is that of `elapsedTime`.
3. `elapsedTime` is set in the previous line.
4. But this depends on the invocation of `doEverySecond`.
5. `doEverySecond` is passed inside a _string_ parameter to `setInterval` inside `startTimer`.
6. `startTimer` is called by the `onload` handler... so it appears that's where the value comes from.
7. Is that it? No, there's also the initialization of the variable `elapsedTime` at the top.
8. Oh wait: `elapsedTime` is also set in `resetElapsed`.
9. Does `resetElapsed` execute? Yes, it is invoked in the `onclick`.

"Just to understand this tiny program," they argue, "the developer needs to reason about timers, initialization,
overlap, interference, and the structure of callbacks." Besides being complex, the program also contains a bug. When the user hits the reset button, the result isn't propagated to the screen until the next call
to `doEverySecond`.

Overall, I agree with this part of the argument. The code as written is hard to understand. The use
of code within strings makes it difficult to read, and the DOM mutations are hard to reason about.
The Flapjax authors go on to blame _callbacks_ for this complexity. Specifically, they argue that
the fact that `doEverySecond`, `startTimer`, and `resetElapsed` are all callbacks makes the code
hard to read. Are callbacks really the problem? Let's see what this code would look like in Solid.

```tsx
function App() {
  const [elapsedTime, setElapsedTime] = createSignal(0);

  const doEverySecond = () => {
    setElapsedTime((elapsedTime) => elapsedTime + 1);
  };

  setInterval(() => doEverySecond(), 1000);

  const resetElapsed = () => {
    setElapsedTime(0);
  };

  return (
    <>
      <button onClick={() => resetElapsed()}>Reset</button>
      <div>{elapsedTime()}</div>
    </>
  );
}
```

Does the same chain of reasoning apply?

1. The value is ostensibly displayed by the second line of the function `doEverySecond`. **No, the
   DOM mutation has been replaced by a combination of signals and JSX.**
2. The value displayed is that of `elapsedTime`. **Yes.**
3. `elapsedTime` is set in the previous line. **Yes.**
4. But this depends on the invocation of `doEverySecond`. **Yes.**
5. `doEverySecond` is passed inside a _string_ parameter to `setInterval` inside `startTimer`.
   **No, it's passed as a normal callback. `startTimer` isn't needed, because everything in the
   function body is called on load.**
6. `startTimer` is called by the `onload` handler... so it appears that's where the value comes
   from. **No.**
7. Is that it? No, there's also the initialization of the variable `elapsedTime` at the top. **Yes.**
8. Oh wait: `elapsedTime` is also set in `resetElapsed`. **Yes.**
9. Does `resetElapsed` execute? Yes, it is invoked in the `onclick`. **Yes.**

In my opinion, a more accurate reading of this function is:

1. The value displayed is that of `elapsedTime`.
2. `elapsedTime` is initialized to 0.
3. By looking for `setElapsedTime` calls, we see that `doEverySecond` and `resetElapsed` update `elapsedTime`.
4. `doEverySecond` increments `elapsedTime`.
5. `doEverySecond` is called every second by `setInterval`.
6. `resetElapsed` resets `elapsedTime` to 0.
7. The DOM contains a button that calls `resetElapsed` when clicked.

Notice also that the bug is not present in the Solid version, since the rendering logic is handled by JSX and the
`elapsedTime` signal.

Let's compare this to Flapjax's solution. Flapjax uses _behaviors_ (with the `B` suffix) and _event streams_ (with the `E` suffix). "A behavior is like a variable -- it always has a
value -- except that changes to its value propagate automatically; an event stream is a
potentially infinite stream of discrete events whose new events trigger additional computation." (To enhance readability, I renamed some of the variables that were shortened in
the paper.):

```js
// a behavior that updates every second
var nowB = timerB(1000);

// a snapshot of the behavior’s value at the time it is invoked, i.e. it _does not_ update automatically
var startTime = nowB.valueNow();

// $E("reset", "click"): event stream of clicks
// snapshotE(nowB): converts the event stream into an event stream of behavior values sampled from nowB
// startsWith(startTime): converts event stream into behavior initialized with startTime
var clickTimesB = $E("reset", "click").snapshotE(nowB).startsWith(startTime);

// difference between behaviors. updated every time either behavior updates
var elapsedB = nowB - clickTimesB;

// insert value into the DOM
insertValueB(elapsedB, "currTime", "innerHTML");

<body onload="loader()">
  <input id="reset" type="button" value="Reset" /> <div id="currTime"> </div>
</body>;
```

A behavior analogous to a signal, and an event stream is analogous to an event handler. To demonstrate
this, we can convert the Flapjax example to Solid code. Every time we see a _behavior_ in the
Flapjax code, we'll use a signal.
Every time we see an _event stream_ we'll use an event handler.

```tsx
// a signal that emits the current time every `interval` milliseconds
function timer(interval: number) {
  const [timer, setTimer] = createSignal(Date.now());

  setInterval(() => setTimer(Date.now()), interval);

  return timer;
}

function App() {
  // var nowB = timerB(1000);
  const now = timer(1000);

  // var startTime = nowB.valueNow();
  // (this translates to just calling the signal directly rather than creating a derived signal)
  const startTime = now();

  // var clickTimesB = $E("reset", "click").snapshotE(nowB).startsWith(startTime);
  // We don't define the event handler here. Notice that if we had more than one event handler,
  //   Flapjax would require us to define all of them up front and merge them together.
  // This part actually covers:
  // var clickTimesB = ....startsWith(startTime);
  const [clickTimes, setClickTimes] = createSignal(startTime);

  // var elapsedB = nowB - clickTimesB;
  // Notice that elapsedB is a behavior, so it becomes a derived signal
  const elapsed = () => Math.floor((now() - clickTimes()) / 1000);

  // var clickTimesB = $E("reset", "click").snapshotE(nowB).startsWith(startTime);
  // This line covers:
  // $E("reset", "click").snapshotE(nowB)
  const reset = () => {
    setClickTimes(now());
  };

  return (
    <>
      <button onClick={reset}>Reset</button>
      {/* insertValueB(elapsedB, "currTime", "innerHTML"); */}
      <div>{elapsed()}</div>
    </>
  );
}
```

Notice the big difference between the Flapjax and Solid versions is where event streams/handlers are
placed. Flapjax positions event streams locally to the behaviors they control. The advantage of this
approach is that a behavior's dependencies can be read directly off the code. However, it obscures
the flow of control. Consider this line:

```tsx
$E("reset", "click").snapshotE(nowB).startsWith(startTime);
```

It affords the following reading: "Reset button click events are converted into a stream of `nowB`
events, initialized with `startTime`."

The Solid version consists of these pieces of code:

```tsx
const [clickTimes, setClickTimes] = createSignal(startTime);
```

```tsx
const reset = () => {
  setClickTimes(now());
};
```

```tsx
<button onClick={reset}>Reset</button>
```

This code affords the following reasoning: "There is a signal called `clickTimes` that is
initialized with `startTime`. When the reset button is clicked, `clickTimes` is updated with the
current time."

Notice the subtle difference here. The Flapjax code is phrase as _push-only_. The button click _flows_
into the snapshot stream modifier, which _flows_ into the initializer. But this doesn't match the
actual data flow pattern which is _push and pull_. `clickTimes` is initialized. The `reset` event _pushes_ an
update to `clickTimes` by _pulling_ `now`. I think the Solid model matches my mental model of the
control flow a lot better.
