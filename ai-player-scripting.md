# :technologist: AI Player Scripting

Consult this FAQ for help with scripting your player and setting up your programming environment.

## :hammer_and_wrench: Programming Environment

Consult this section for setting up your programming environment.

### What programming language do I script my player in?

When you sign up you are given a choice between [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) and [TypeScript](https://www.typescriptlang.org).

### Which programming language is a better choice for me?

If you're rather new to programming or prefer to program without types, choose JavaScript. If you prefer to have your code typed for better error detection, choose TypeScript.

### What IDE _(Integrated Development Environment)_ do I use?

Any IDE that supports JavaScript or TypeScript is perfectly acceptable to use.

Sample IDEs:

- [JetBrains Fleet](https://www.jetbrains.com/fleet)

- [IntelliJ IDEA](https://www.jetbrains.com/idea)

- [Sublime Text](https://www.sublimetext.com)

- [Visual Studio Code](https://code.visualstudio.com)

- [WebStorm](https://www.jetbrains.com/webstorm)

- [Zed](https://zed.dev)

### Does the competition software's runtime support IDE debuggers?

No, that was out of scope for the software.

### How do I configure my IDE for the competition software's runtime?

Make sure that the supplied `jsconfig.json` (or `tsconfig.json`, if using TypeScript) file in the root of your workspace. Then also make sure that `lib.stdlib.d.ts` and `lib.dotsandboxes.d.ts` exist in your workspace root as well.

These files tell your IDE what types, globals, and language support is available in the runtime.

> **TODO:** Pictures here showing a JavaScript and TypeScript root directory.

### Do I have to use an IDE?

No, any text editor is fine. When you use an IDE you get nice features like variable completions and real-time type checking.

Sample Text Editors:

- [emacs](https://www.gnu.org/software/emacs)

- [GNU nano](https://nano-editor.org) _(based)_

- [Notepad++](https://notepad-plus-plus.org)

- [Vim](https://www.vim.org) _(ew)_

- [Windows Notepad](https://en.wikipedia.org/wiki/Windows_Notepad)

### What text editors should I avoid, if any?

Any text editor that supports rich text will mangle your source code.

Sample Rich Text Editors:

- [LibreOffice](https://www.libreoffice.org)

- [macOS TextEdit](https://support.apple.com/guide/textedit/welcome/mac)

  - **NOTE**: TextEdit can have its rich text mode disabled. Please consult its documentation.

- [OnlyOffice](https://www.onlyoffice.com)

- [Microsoft Word](https://www.microsoft.com/en-us/microsoft-365/word)

- [Windows Wordpad](https://en.wikipedia.org/wiki/WordPad)

### What operating systems are supported by the competition software's runtime?

Linux, macOS, and Windows are all supported.

### How do I download the competition software's runtime?

Head over to [github.com/PSH-Computing-AI-club/competition-spring-2025-dotsandboxes/releases](https://github.com/PSH-Computing-AI-club/competition-spring-2025-dotsandboxes/releases) and download the latest CLI binary that matches your operating system.

Download the binary to the root of your workspace.

> **TODO:** Video of doing just that and bypassing Microsoft Edge's filters.

## :books: Documentation

Consult this section for learning material regarding programming and the competition software's runtime.

### What resources are there for JavaScript?

Generally, the Internet, Reddit, YouTube, and so on have a plethora of resources available to help you learn JavaScript. Please consult those.

I highly recommend the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript), or MDN. It contains high quality guides and reference material for the JavaScript standard. Also known as ECMAScript.

### What resources are there for TypeScript?

Like above with JavaScript please consult the wider Internet.

I highly recommend the [official TypeScript Documentation](https://www.typescriptlang.org/docs). It contains high quality guides and reference material.

### Where can I find the competition software's runtime API documentation?

The API documentation for the runtime can be found at [`psh-computing-ai-club.github.io/competition-spring-2025-dotsandboxes`](https://psh-computing-ai-club.github.io/competition-spring-2025-dotsandboxes).

## :writing_hand: Programming Your Player

Consult this section for programming your player.

### How do I get started with scripting my player?

After cloning your supplied git repository, open the root workspace directory in your preferred editor.

> **TODO:** Picture of VS Code opened.

Then open the `mod.js` (or `mod.ts`, if using TypeScript) file. This is your AI player.

> **TODO:** VS Code with file open.

As you can see, there is an [arrow function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) (similar to [lambda expressions](https://docs.python.org/3/tutorial/controlflow.html#lambda-expressions) in Python) being [exported as the default](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) export. This is your compute function.

> **TODO:** VS Code highlight function.

You program the AI logic of your player here.

### How do I make a move?

Simply return an [`object`](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Object_basics) with `.x` and `.y` coordinate fields.

> **TODO:** VS Code programming a simple object.

### How do I forfeit a game session?

Simply return a [`null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) value.

### Should I always have a return value?

Yes! If the logic you wrote for your compute function cannot find a valid move, then return a `null` value.

### How do I run and test my player?

> **NOTE:** Swap `./dotsandboxes-linux` for `./dotsandboxes-macos` or `./dotsandboxes-windows.exe` if you are using either of those operating systems instead.

> **NOTE:** Swap the `.js` file extension for `.ts` if using TypeScript instead.

Run the competition software with `./dotsandboxes-linux simulate ./mod.js ./random_player.js` in a terminal with its directory set to your workspace's root directory.

This will pit your AI player versus the supplied sample random player.

> **TODO:** Video of this.

### How do I implement strategies?

That is entirely up to you. The competition software's runtime provides a plethora of APIs for you to utilize. Check out the supplied sample `strategic_player.js` (or `strategic_player.ts`, if using TypeScript) for a sample implementation.

### Each run of the competition software is random. How can I prevent this?

> **NOTE:** Swap `./dotsandboxes-linux` for `./dotsandboxes-macos` or `./dotsandboxes-windows.exe` if you are using either of those operating systems instead.

By default, the competition software uses the amount of milliseconds since the [UNIX Epoch](https://en.wikipedia.org/wiki/Unix_time) as the seed for randomness. If you want to reuse an earlier seed or your own custom one, then supply the `--seed` option like so: `./dotsandboxes-linux simulate --seed {SEED} ...players...`.

> **TODO:**: Video of this.

It is very **IMPORTANT** to understand that you _will not_ control the seed during the practice nor final tournament brackets.

### Can I change the grid size of the game board?

By default, the competition software uses 5 columns and 3 rows as the grid size. If you want to change this, then simply supply the `--grid-columns` and `--grid-rows` options respectively like so: `./dotsandboxes-linux simulate --grid-columns {COLUMNS} --grid-rows {ROWS} ...players...`.

> **TODO:**: Video of this.

It is very **IMPORTANT** to understand that you _will not_ control the grid size during the practice nor final tournament brackets.

### How do I import code files?

Simply use the [import declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) at the top of your player file and [export declaration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export) in the imported file. Check out the supplied sample `strategic_player.js` (or `strategic_player.ts`, if using TypeScript) and `common.js` (or `common.ts`, if using TypeScript) for a sample implementation.

### How can I find out if my player has a parsing error?

Currently, due to limitations, the competition software **DOES** output syntax errors but with unhelpful stack traces.

It is recommended to use an IDE or a separate analysis tool to help find syntax errors.

### How can I find out if my player throws a runtime error?

Anytime your player has a runtime error due to logic or reference bugs a full stack trace will be printed to console.

**TODO:** Show a video of this.
