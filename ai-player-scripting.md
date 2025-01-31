# :technologist: AI Player Scripting

Consult this FAQ for help with scripting your player and setting up your programming environment.

- [:technologist: AI Player Scripting](#technologist-ai-player-scripting)
  - [1. :hammer\_and\_wrench: Programming Environment](#1-hammer_and_wrench-programming-environment)
    - [1.1. What programming language do I script my player in?](#11-what-programming-language-do-i-script-my-player-in)
    - [1.2. Which programming language is a better choice for me?](#12-which-programming-language-is-a-better-choice-for-me)
    - [1.3. What IDE _(Integrated Development Environment)_ do I use?](#13-what-ide-integrated-development-environment-do-i-use)
    - [1.4. Does the competition software's runtime support IDE debuggers?](#14-does-the-competition-softwares-runtime-support-ide-debuggers)
    - [1.5. How do I configure my IDE for the competition software's runtime?](#15-how-do-i-configure-my-ide-for-the-competition-softwares-runtime)
    - [1.6. Do I have to use an IDE?](#16-do-i-have-to-use-an-ide)
    - [1.7. What text editors should I avoid, if any?](#17-what-text-editors-should-i-avoid-if-any)
    - [1.8. What operating systems are supported by the competition software's runtime?](#18-what-operating-systems-are-supported-by-the-competition-softwares-runtime)
    - [1.9. How do I download the competition software's runtime?](#19-how-do-i-download-the-competition-softwares-runtime)
  - [2. :books: Documentation](#2-books-documentation)
    - [2.1. What resources are there for JavaScript?](#21-what-resources-are-there-for-javascript)
    - [2.2. What resources are there for TypeScript?](#22-what-resources-are-there-for-typescript)
    - [2.3. Where can I find the competition software's runtime API documentation?](#23-where-can-i-find-the-competition-softwares-runtime-api-documentation)
  - [3. :writing\_hand: Programming Your Player](#3-writing_hand-programming-your-player)
    - [3.1. How do I get started with scripting my player?](#31-how-do-i-get-started-with-scripting-my-player)
    - [3.2. How do I make a move?](#32-how-do-i-make-a-move)
    - [3.3. How do I forfeit a game session?](#33-how-do-i-forfeit-a-game-session)
    - [3.4. Should I always have a return value?](#34-should-i-always-have-a-return-value)
    - [3.5. How do I run and test my player?](#35-how-do-i-run-and-test-my-player)
    - [3.6. Do I need an internet connection to run the competition software?](#36-do-i-need-an-internet-connection-to-run-the-competition-software)
    - [3.7. How do I implement strategies?](#37-how-do-i-implement-strategies)
    - [3.8. Each run of the competition software is random. How can I prevent this?](#38-each-run-of-the-competition-software-is-random-how-can-i-prevent-this)
    - [3.9. Can I change the grid size of the game board?](#39-can-i-change-the-grid-size-of-the-game-board)
    - [3.10. How do I import code files?](#310-how-do-i-import-code-files)
    - [3.11. How can I find out if my player has a parsing error?](#311-how-can-i-find-out-if-my-player-has-a-parsing-error)
    - [3.12. How can I find out if my player throws a runtime error?](#312-how-can-i-find-out-if-my-player-throws-a-runtime-error)
    - [3.13. Will I be given error logs when the competition software runs my code?](#313-will-i-be-given-error-logs-when-the-competition-software-runs-my-code)

## 1. :hammer_and_wrench: Programming Environment

Consult this section for setting up your programming environment.

### 1.1. What programming language do I script my player in?

When you sign up you are given a choice between [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) and [TypeScript](https://www.typescriptlang.org).

### 1.2. Which programming language is a better choice for me?

If you're rather new to programming or prefer to program without types, choose JavaScript. If you prefer to have your code typed for better error detection, choose TypeScript.

### 1.3. What IDE _(Integrated Development Environment)_ do I use?

Any IDE that supports JavaScript or TypeScript is perfectly acceptable to use.

Sample IDEs:

- [JetBrains Fleet](https://www.jetbrains.com/fleet)

- [IntelliJ IDEA](https://www.jetbrains.com/idea)

- [Sublime Text](https://www.sublimetext.com)

- [Visual Studio Code](https://code.visualstudio.com)

- [WebStorm](https://www.jetbrains.com/webstorm)

- [Zed](https://zed.dev)

### 1.4. Does the competition software's runtime support IDE debuggers?

No, that was out of scope for the software.

### 1.5. How do I configure my IDE for the competition software's runtime?

Make sure that the supplied `jsconfig.json` (or `tsconfig.json`, if using TypeScript) file in the root of your workspace. Then also make sure that the `lib.stdlib.d.ts` and `lib.dotsandboxes.d.ts` files exist in your workspace root as well.

These files tell your IDE what types, globals, and language support is available in the runtime.

> **TODO:** Pictures here showing a JavaScript and TypeScript root directory.

### 1.6. Do I have to use an IDE?

No, any text editor is fine. When you use an IDE you get nice features like variable completions and real-time type checking.

Sample Text Editors:

- [emacs](https://www.gnu.org/software/emacs)

- [GNU nano](https://nano-editor.org) _(based)_

- [Notepad++](https://notepad-plus-plus.org)

- [Vim](https://www.vim.org) _(ew)_

- [Windows Notepad](https://en.wikipedia.org/wiki/Windows_Notepad)

### 1.7. What text editors should I avoid, if any?

Any text editor that supports rich text will mangle your source code.

Sample Rich Text Editors:

- [LibreOffice](https://www.libreoffice.org)

- [macOS TextEdit](https://support.apple.com/guide/textedit/welcome/mac)

  - **NOTE**: TextEdit can have its rich text mode disabled. Please consult its documentation.

- [OnlyOffice](https://www.onlyoffice.com)

- [Microsoft Word](https://www.microsoft.com/en-us/microsoft-365/word)

- [Windows Wordpad](https://en.wikipedia.org/wiki/WordPad)

### 1.8. What operating systems are supported by the competition software's runtime?

Linux, macOS, and Windows are all supported.

### 1.9. How do I download the competition software's runtime?

Head over to [github.com/PSH-Computing-AI-club/competition-spring-2025-dotsandboxes/releases](https://github.com/PSH-Computing-AI-club/competition-spring-2025-dotsandboxes/releases) and download the latest CLI binary that matches your operating system.

Download the binary to the root of your workspace.

> **TODO:** Video of doing just that and bypassing Microsoft Edge's filters.

## 2. :books: Documentation

Consult this section for learning material regarding programming and the competition software's runtime.

### 2.1. What resources are there for JavaScript?

Generally, the Internet, Reddit, YouTube, and so on have a plethora of resources available to help you learn JavaScript. Please consult those.

I highly recommend the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript), or MDN. It contains high quality guides and reference material for the JavaScript standard. Also known as ECMAScript.

### 2.2. What resources are there for TypeScript?

Like above with JavaScript please consult the wider Internet.

I highly recommend the [official TypeScript Documentation](https://www.typescriptlang.org/docs). It contains high quality guides and reference material.

### 2.3. Where can I find the competition software's runtime API documentation?

The API documentation for the runtime can be found at [`psh-computing-ai-club.github.io/competition-spring-2025-dotsandboxes`](https://psh-computing-ai-club.github.io/competition-spring-2025-dotsandboxes).

## 3. :writing_hand: Programming Your Player

Consult this section for programming your player.

### 3.1. How do I get started with scripting my player?

After cloning your supplied git repository, open the root workspace directory in your preferred editor.

https://github.com/user-attachments/assets/eff1605f-6705-48b9-bbbc-60717a5f93a1

> Opening VS Code by the "Open Folder" menu options.

https://github.com/user-attachments/assets/889a26d3-17a9-4e95-8273-4f3e68cbd079

> Opening VS Code by your file explorer.

https://github.com/user-attachments/assets/bd6d8ec4-3edb-48df-8d50-edfee346509e

> Opening VS Code by using the change directory command.

Then open the `mod.js` (or `mod.ts`, if using TypeScript) file. This is your AI player.

![The `mod.js` entry point open in VS Code.](./.assets/demo.vscode.entry-point.jpg)

As you can see, there is an [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) (similar to [lambda expressions](https://docs.python.org/3/tutorial/controlflow.html#lambda-expressions) in Python) being [exported as the default](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) export. This is your compute function.

![The compute function highlighted in VS Code.](./.assets/demo.vscode.compute-function.jpg)

You program the AI logic of your player here.

### 3.2. How do I make a move?

Simply return an [`object`](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics) with `.x` and `.y` coordinate fields.

https://github.com/user-attachments/assets/cb9adbc1-2754-4128-bd5a-95948945492e

### 3.3. How do I forfeit a game session?

Simply return a [`null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) value.

### 3.4. Should I always have a return value?

Yes! If the logic you wrote for your compute function cannot find a valid move, then return a `null` value.

### 3.5. How do I run and test my player?

> [!NOTE]
> Swap `./dotsandboxes-linux` for `./dotsandboxes-macos` or `./dotsandboxes-windows.exe` if you are using either of those operating systems instead.

> [!NOTE]
> Swap the `.js` file extension for `.ts` if using TypeScript instead.

Run the competition software with `./dotsandboxes-linux simulate ./mod.js ./random_player.js` in a terminal with its directory set to your workspace's root directory.

This will pit your AI player versus the supplied sample random player.

https://github.com/user-attachments/assets/9f847979-3239-4c7b-a713-09cc227cf092

### 3.6. Do I need an internet connection to run the competition software?

Yes, for the first run only. The competition software uses the [`denoland/deno_emit`](https://github.com/denoland/deno_emit) library is used to prepare your JavaScript and TypeScript code for running in the scripting runtime. It is a bundling and transpilation library made in [Rust](https://www.rust-lang.org) compiled to [WebAssembly](https://developer.mozilla.org/en-US/docs/WebAssembly). Unfortunately, the library does not ship with its WASM payload and downloads it on first run. Our apologies if this is inconvenient for you.

### 3.7. How do I implement strategies?

That is entirely up to you. The competition software's runtime provides a plethora of APIs for you to utilize. Check out the supplied sample `strategic_player.js` (or `strategic_player.ts`, if using TypeScript) for a sample implementation.

### 3.8. Each run of the competition software is random. How can I prevent this?

> [!NOTE]
> Swap `./dotsandboxes-linux` for `./dotsandboxes-macos` or `./dotsandboxes-windows.exe` if you are using either of those operating systems instead.

By default, the competition software uses the amount of milliseconds since the [UNIX Epoch](https://en.wikipedia.org/wiki/Unix_time) as the seed for randomness. If you want to reuse an earlier seed or your own custom one, then supply the `--seed` option like so: `./dotsandboxes-linux simulate --seed {SEED} ...players...`.

> **TODO:**: Video of this.

It is very **IMPORTANT** to understand that you _will not_ control the seed during the practice nor final tournament brackets.

### 3.9. Can I change the grid size of the game board?

By default, the competition software uses 5 columns and 3 rows as the grid size. If you want to change this, then simply supply the `--grid-columns` and `--grid-rows` options respectively like so: `./dotsandboxes-linux simulate --grid-columns {COLUMNS} --grid-rows {ROWS} ...players...`.

> **TODO:**: Video of this.

It is very **IMPORTANT** to understand that you _will not_ control the grid size during the practice nor final tournament brackets.

### 3.10. How do I import code files?

Simply use the [import declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) at the top of your player file and [export declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) in the imported file. Check out the supplied sample `strategic_player.js` (or `strategic_player.ts`, if using TypeScript) and `common.js` (or `common.ts`, if using TypeScript) for a sample implementation.

### 3.11. How can I find out if my player has a parsing error?

Currently, due to limitations, the competition software **DOES** output syntax errors but with unhelpful stack traces.

It is recommended to use an IDE or a separate analysis tool to help find syntax errors.

### 3.12. How can I find out if my player throws a runtime error?

Anytime your player has a runtime error due to logic or reference bugs a full stack trace will be printed to console.

**TODO:** Show a video of this.

### 3.13. Will I be given error logs when the competition software runs my code?

Due to time constraints, the competition software's tournament bracket landing page will not report error logs.

However, the raw JSON logs will be available for download upon request. Please contact a competition organizer for more information.
