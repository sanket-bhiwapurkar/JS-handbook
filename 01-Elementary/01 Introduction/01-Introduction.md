# Questions 

- 01 What is JS?
- 02 What are the features of JS?
- 03 What does it mean that JS is a scripting language?
- 04 What is a JS Engine?
- 05 What are the Key JavaScript Engines?
- 06 How JavaScript Engines Improve Performance?

Definition,

## What is `JavaScript` ?

- JavaScript is a `high-level`, `interpreted`, and `dynamic` programming language (Mnemonics: HID)
- primarily used for creating `interactive` and `dynamic` web pages. (Mnemonics: ID)
- It is a `core technology` of the `World Wide Web`, alongside `HTML` and `CSS`, enabling `client-side scripting`. (Mnemonics: CWC)

## What are the `features` of JavaScript? (Mnemonics: EVACI)

- JavaScript allows developers to implement complex features such as:

  - **Event handling**: JavaScript can respond to `user actions` such as `clicks`, `keypresses`, and `mouse movements`, creating a more interactive `experience`.

  - **Versatility**: JavaScript is used for a wide range of `applications`, from building `web` applications to `serve-side` programming, `mobile apps`, and even `desktop applications`.

  - **Asynchronous programming**: With features like `Promises` and `async/await`, JavaScript can handle asynchronous tasks like fetching data from a server `without blocking the main thread`, improving `performance` and user `experience`.

  - **Cross-platform**: JavaScript `runs on all` modern web `browsers` and is also used in `server-side development` (Node.js), enabling developers to use a `single language for both` client and server-side code.

  - **Interactivity**: JavaScript enables features like form `validation`, `animations`, `dynamic content updates`, and `user interactions` on web pages.

Overall, JavaScript is essential for modern web development, providing rich functionality and enhancing user experience.

## What does it mean that JS is a `scripting language`? (Mnemonics: DIANE)

- When JavaScript (JS) is referred to as a scripting language, it means that it is designed primarily for `writing scripts` to `automate` tasks or `control` the behavior of a program,
- often within the `context` of a `web browser` or `server-side environment`.
- Here’s what that implies:

  - **Dynamic and Lightweight**: JavaScript scripts are often `smaller` in size and written to perform `specific` tasks `quickly`, rather than building `large`, complex systems from `scratch`. This allows for `rapid development` and `easy integration` with web `pages` and web `applications`.

  - **Interpreted Language**: JavaScript is `not compiled` into machine code like some other languages (e.g., C++). Instead, it is `interpreted` by a JavaScript `engine` (such as V8 in Chrome) at runtime. This means that JavaScript code is `executed directly`, `without` the need for a `separate compilation step`, making it `easier` to `test and debug`.

  - **Automates Actions**: As a scripting language, JavaScript is typically used to `write small programs` or `scripts` that `automate` or `control` specific `tasks`. For example, it can automate user `interactions` on a webpage (like responding to clicks), `modify` the content on the page dynamically, or `communicate with servers` to `fetch` or send `data` without refreshing the page.

  - **Not Typically Used for System-Level Programming**: While languages like C++ or Java are used to develop `system` software, `operating systems`, or applications with `high-performance` requirements, JavaScript is generally used for creating `web-based applications` or `automating tasks` in a `less resource-intensive` environment.

  - **Embedded in Other Software**: JavaScript is often `embedded within other programs` (like a web browser), and it `enhances` or `controls` the `behavior` of those programs. For example, JavaScript can `interact` with the Document Object Model `(DOM)` in browsers, `modifying` the content and structure of `web pages` in real-time.

In summary, calling JavaScript a "scripting language" emphasizes its role in automating tasks, interacting with web elements, and enabling dynamic behaviors in web pages, rather than being used for large-scale software development or system programming.

## What are JS `Engines`?

- A JavaScript engine is a `program` or an `interpreter` that `executes` JavaScript code.
- It `reads` the JavaScript code and `converts` it into `machine code` that the computer can `understand` and `execute`.
- JavaScript engines are `embedded` in web browsers, allowing them to `run` JavaScript code on `web pages`,
- but they are also used in `other environments` like `Node.js` for `server-side` programming.

Here’s a breakdown of how JavaScript engines work:

- Parsing: The engine `reads` the JavaScript code and `breaks it down` into `smaller` pieces, known as `tokens`. It then `parses` these tokens into a `data structure` called an `Abstract Syntax Tree (AST)` that `represents` the `code's logical structure`.

- Compilation/Interpretation:

  - `Traditionally`, JavaScript engines would interpret the code `line-by-line`, meaning they would translate it `directly` into `machine code` as the program ran.
  - `Modern engines` often use a `technique` called Just-In-Time `(JIT)` Compilation, where the JavaScript code is compiled into machine code at `runtime`, which is then executed for `faster performance`.

## What are the Key JavaScript `Engines`?

1. **V8** (Chrome, Node.js):
   - Developed by Google for Chrome and used in Node.js, V8 is one of the most popular and widely-used JavaScript engines. It uses JIT compilation to speed up code execution by compiling JavaScript into machine code.
2. **SpiderMonkey** (Firefox):

   - Developed by Mozilla, SpiderMonkey is the JavaScript engine used in Firefox. It also employs JIT compilation for improved performance.

3. **JavaScriptCore** (Safari):

   - Also known as _Nitro_, this is the JavaScript engine used in Safari (Apple’s web browser). Like V8 and SpiderMonkey, it utilizes JIT compilation.

4. **Chromium** (Edge, older versions):

   - Chakra was the JavaScript engine used by Microsoft’s Edge browser before it switched to Chromium. It also supports JIT compilation for faster execution.

5. **Hermes** (React Native):
   - Hermes is an open-source JavaScript engine optimized for running on mobile devices, particularly in React Native applications, where performance and memory usage are key concerns.

## How JavaScript `Engines` Improve `Performance` (Mnenomics: JOG)?

- **JIT Compilation**: Modern engines use `JIT compilation` to `convert` JavaScript into machine code right `before it is executed`, `rather` than interpreting it `line-by-line`. This `reduces the time` it takes to `run` JavaScript code, especially for larger scripts.
- **Optimization**: JavaScript engines optimize commonly-used `functions` and `patterns`, such as `recognizing repeated code` and optimizing it for faster execution.

- **Garbage Collection**: JavaScript engines `manage memory` through garbage collection, `automatically cleaning` up memory that's no longer in use, which helps prevent `memory leaks`.
