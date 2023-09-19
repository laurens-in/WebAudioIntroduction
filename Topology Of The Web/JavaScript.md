JavaScript is the programming language of [[the web]]. Before it was created, there were Java Applets and Adobe Flash. Before that the web was completely static.

This is en example of how it can look like:

```js
const threshold = 0.8

function randomDecider(thresh) {
  const randomFloat = Math.random();
  if (randomFloat > thresh) return true;
  if (randomFloat <= thresh) return false;
}

console.log(randomDecider(threshold));
```

JavaScript is a just-in-time-compiled scripting language.

What does that mean? Computers only understand machine-code. Every program has to be translated to machine-code in order to run. Some languages, like C or Rust, are compiled. This means that the code is transformed (compiled) into an executable binary of machine-code, before it is executed. JavaScript works differently. We have a runtime that reads lines of JavaScript code (inside the browser or Node.js) and translates them to machine-code on the fly. This runtime of course introduces a performance and memory overhead, but it also allows us to be much more flexible. At any more code can be thrown at the runtime and executed.

As a language designed primarily for working with user-interfaces it is designed around the following principles:

- event-loop
- asynchronous  (useful for I/O)
- single-threaded
- multi-paradigm

If these words mean nothing to you right now, don't worry. We will look at JavaScript and some of these things in more detail during this course.
