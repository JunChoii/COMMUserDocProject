# Introduction

This page is to draw and introduce you into the basic idea of [Fetch API](#fetch-api). It provides users the interface that fetches elements like, responses and requests that organizes HTTP pipeline. You can access and control it from JavaScript.
You can also fetch network resources through `fetch()` method that Fetch API supports.

## Introducing Fetch API

We used to be able to commit those functionality by using `XMLHttpRequest`. However, fetch API is much better alternative as well as that easily being used in other different environments.

### Background

#### Why it is necessary

Let's say you are doing HTML. You use `<a href="">` to give users `url` to allow them to move to the other page. However, this way causes blinking the window which means it reloads every time user clicks on `<a href="">` and also in case you load some huge data from it, it will take long to get it you. Plus, it reloads the whole page every time including the same tag which is not necessary.

More than that, JavaScript is single threaded language so it should run the whole things through one thread. To improve such difficulty, [`Asynchronous`](#asynchronous) communication became important.

#### Promise

Promise is an object that JavaScript provides to help you run your code `Asynchronously`. The reason why Promise showed up here is that it is directly related to network communication and [`Asynchronous`](#asynchronous) way of coding. Promise run the function that you asked it to, and then, it returns results depending on the function is failed or succeeded. And the result that `fetch()` returns is promise.

```javascript
const promise = new Promise((resolve, reject) => {
  console.log("Want to be a Full Stack Webdeveloper?....Really?");
  setTimeout(() => {
    resolve("data");
  }, 1000);
});
```

In promise, you pass in two parameters in the callback function:

resolve - runs the function successfully and returns data. Recieves the result using `.then()`

reject - if there is an error running the function, reject is called and get error result using `.catch()`

#### Fetch Syntax

```javascript
fetch(url, options)
  .then((response) => console.log("response:", response))
  .catch((error) => console.log("error:", error));
```

You see the similarity between `fetch` and `promise`?

Now, in the next page, let's go through how to actually use `fetch()`.
