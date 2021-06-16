# RxJS Interview Questions & Answers 🌹 [![GitHub](https://img.shields.io/github/license/nikhilrstg18/iq?color=blue)](https://github.com/nikhilrstg18/iq/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/nikhilrstg18/iq) ![GitHub forks](https://img.shields.io/github/forks/nikhilrstg18/iq)

> Click :star: if you like the project. Pull Requests are highly appreciated.

> [![Twitter](https://img.shields.io/twitter/follow/rustagi_nikhil?label=Follow%20%40rustagi_nikhil&style=social)](https://twitter.com/rustagi_nikhil) for technical updates.

---

## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---

### Table of Contents

| No. | Questions                                                                                                                                   |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is **RxJS** ?](#What-is-RxJS)                                                                                                         |
| 2   | [Why use RxJS instead of **callbacks**, **Promise**, **async**/**await** ?](#Why-use-RxJS-instead-of-`callbacks`,-`Promise`,-`async/await`) |
| 3   | [Angular uses RxJS, How is RxJS used in Angular ?](#Angular-uses-RxJS,-How-is-RxJS-used-in-angular)                                         |
| 4   | [What is **Reactive Development** ?](#What-is-Reactive-Development)                                                                         |

---

---

1. ### What is RxJS

   RxJS is short for Reactive Extension for JS

   Acc. to [doc](https://rxjs.dev/guide/overview)

   > RxJS is a library for composing asynchronous and event-based programs by using **observable sequences**

   Observable sequences ?

   Think of it as `Manage Data as it flows through time` - Collect, Pipe, Combine, Cache

   > RxJS is a library for composing obseravable streams and optionally processing each item in the stream using extensive set of operators

   **[⬆ Back to Top](#table-of-contents)**

2. ### Why use RxJS instead of `callbacks`, `Promise`, `async/await`

   There are other techniques to manage async data like

   1. **callbacks:**

      - A Callback is a function that can be called back, when an async operation is complete.
      - A Callback is difficult to manage when there are nested async operations.

      ```javascript
      var cb = () => console.log("calledback");
      var myFunc = (cb) => cb();
      ```

   2. **Promise:**

      - A Promise is an object and can only handle `single emission`
      - It has 2 chainable handling methods `.then()` and `.catch()`
      - It is `not cancellable`
      - Promises are `eager loaded`

      ```javascript
      let myPromise = new Promise(function (myResolve, myReject) {
        setTimeout(function () {
          myResolve("Hello Youtube !!");
        }, 3000);
      });

      myPromise.then(function (value) {
        console.log(value);
      });
      ```

      - Promise has 2 properties : `state` and `result`

        | myPromise.state | myPromise.result |
        | --------------- | ---------------- |
        | **pending**     | undefined        |
        | **resolved**    | a result value   |
        | **rejected**    | an error object  |

   3. **async/await:**

      - async and await is sugar syntax allows us to write async code that also can handle single emission
      - It is `not cancallable`
      - async and await make promises easier to write

      The keyword `async` before a function makes the function return a promise:

      ```javascript
      async function myFunction() {
        return "Hello";
      }
      ```

      is same as

      ```javascript
      async function myFunction() {
        return Promise.resolve("Hello");
      }
      ```

      The keyword `await` before a function makes the function wait for a promise

      ```javascript
      let result = await myFunction();

      console.log(
        "This line is executed after 3 sec with awaited result",
        result
      );
      ```

   4. **RxJS:**

      - RxJS provides a `single technique and operators` for working with any type of data
        (often work with multiple sources of data i.e. events from keyboards, mouse, routes or data from database, 3rd party APIs, etc.
      - RxJS is `Compositional` i.e. we can easily compose data from different source to feed our view.
      - RxJS is `Watchfull` i.e. RxJS can produce multiple values overtime and makes use of Push-Model approach to notify your code when specific action occur, making it wasy to react to events and data changes.
      - RxJS is `Lazy` i.e. evaluation doesn't start until subscription. So we can create recepies that can execute when we need the result
      - RxJS has `built-in Error handling` i.e. for better user experience
      - RxJS is `Cancellable` for eg. if user click on product A and immediately click on prodcut A, we can cancel the request of product A

      **[⬆ Back to Top](#table-of-contents)**

3. ### Why Angular uses RxJS as core set of lib, How is RxJS used in Angular

   RxJS used in

   - Angular's **Routing** to seek changes in route params, route data and router events.
   - Angular's **Reactive Forms** to seek valueChanges when user modifies the input of the form
   - Angular's **HttpClient** service to communicate with API to receive and send info

   i.e. why RxJS is installed as core set of lib of Angular. We can extend the use of RxJS in our angular app to move towards **Reactive Development**

   **[⬆ Back to Top](#table-of-contents)**

4. ### What is Reactive Development

   Acc. to [wikipedia](https://en.wikipedia.org/wiki/Reactive_programming) Reactive Development aka Reactive Programming is a

   > ...declarative programming paradigm concerned with data streams and the propagation of change

   - As the user makes the selection, data is retreived from backend server or some other system's data changed that change is propagated and the application reacts appropriately (updating the view or performing some other action)
   - Reactive Development is functional, thus you can specifiy the behavior of a value completely at the time of declaration

   Reactive Development is

   - Quick to react to user's interactions
   - Resilient to failures
   - Reactive to state changes, instead of calling callbacks

   **[⬆ Back to Top](#table-of-contents)**
