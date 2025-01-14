# Project Architecture

## Overview

- `.`: Configuration files
- `package.json`: Project settings
- `build/`: Contains generated binaries
- `dist/`: Build files for deployment
- `docs/`: Documentation and assets
- `resources/`: Application assets using at build time
- `node_modules/`: Dependencies
- `src`: Mark Text source code
  - `common/`: Common source files that only require Node.js APIs. Code from this folder can be used in all other folders except `muya`.
  - `main/`: Main process source files that require Electron main-process APIs. `main` files can use `common` source code.
  - `muya/`: Mark Texts backend that only allow pure JavaScript, BOM and DOM APIs. Don't use Electron or Node.js APIs!
  - `renderer`: Frontend that require Electron renderer-process APIs and may use `common` or `muya` source code.
- `static/`: Application assets (images, themes, etc)
- `test/`: Contains (unit) tests

## Introduction to Mark Text

MarkTextCode is a minimal ,  realtime preview (WYSIWYG) editor for markdown along with support of code snippets ( just like jupyter notebook) but keeping the feel of professional docs and support of dynamic runtime enviornments to provide the unique  packaged editor that reduces the need of coder as vim does (by putting all the  vscode bundles accessed by `/<text>` command  along with ```<language>  <code>  ``` for writing  the  runtime scripts). 

Muya provides realtime preview and markdown editing via multiple modules based on diffrent specifications defined (commonMark / Github Flavored Markdown). along with possiblity of providing embedded scripting feature ( supported by wasm ) to run the scripts / embedded  UI components and multimedia as an fluent documentation.  it can be used as multithreaded to boost the performance .

> NOTE: Mark Text's source-code editor is provided by CodeMirror and not well optimized nor feature rich. It's not part of Muya and an editor (renderer process) feature that load the markdown text from Muya (export), operate on it and re-import the text into Muya when switching to preview mode.

> NOTE: Muya requires a core refactoring to provide better modularization, APIs and plugins. Furthermore, the data structure need improvements for better performance and stability.

> NOTE: on the part of new features , [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly/Concepts) is currently in early phase and will  indeed take time for being more portable to run fluently runtime for all languages , but for initial phases , i will develop it to support the snippets for npm , rust runtimes . 


The editor represents the view and is split into two parts. The first is the main process that have full access to Electron and all OS features. It's mainly used for IO, user interaction with native dialogs and controlls the editor windows. The main process should not (be long) blocked by synchronous operations. The renderer process is the real editor and also a host for Muya. It's responsible for all graphical elements (`src/renderer/components`), data (`src/renderer/store`) and data synchronization. A renderer process is spawned for each window, operates on its own and is controlled by the main process. It contains two text editors: the realtime preview editor provided by Muya and the source-code one by CodeMirror with special features such as tabs, sidebar and editing features.

### Application entry points

There are two entry points to the application:

- `src/main/index.js` for the main process that is executed first and only once per instance. Once the application is initialized, it's safe to access all the environment variables and single-instances and the application (`App`) is started (`src/main/app/index.js`). You can use the application after `App::init()` is run successfully.
- `src/renderer/main.js` for each editor window. At the beginning libraries are loaded, the window is initialized and Vue components are mounted.

### How Muya work

TBD

- Overview about Muya components
- How Muya work internal
- Data structure
- And how there will be possible integration of wasm and modules fo rendering the webapp snippets. 

### Main- and renderer process communication

Main- and renderer process communicate asynchronously via [inter-process communication (IPC)](code/IPC.md) and it's mainly used for IO and user interaction with native dialogs.

### Editor window (renderer process)

TBD

### Examples

#### Opening a markdown document and render it

`MarkdownDocument` is a document that represents a markdown file on disk or an untitled document. To get a markdown document you can use the `loadMarkdownFile` function that asynchronously returns a `RawMarkdownDocument` (= `MarkdownDocument` with some additional information) in the main process.

**Overall steps to open a file:**

1. Click `File -> Open File` and a file dialog is shown that emit `app-open-file-by-id` with the editor window id to open the file in and resolved absolute file path.
2. The application (`App` instance) tries to find the specified editor and call `openTab` on the editor window. A new editor window is created if no editor window exists.
3. The editor window tries to load the markdown file via `loadMarkdownFile` and send the result via the `mt::open-new-tab` event to the renderer process.
  - Each opened file is also added to the filesystem watcher and the full path is saved to track opened file in the current editor window.
4. The event is triggered in `src/renderer/store/editor.js` (renderer process), does some checks and create a new document state that represent a markdown document and tab state.
5. The new created tab is either opened and the `file-changed` event is emitted or just added to the tab state.
6. Both Muya and the source-code editor listen on this event and change the markdown document accordingly.

> NOTE: We currently have no high level APIs to make changes to the document text or lines automatically. All modifications need user interaction!


**steps of adding an web assembly VM:**

TODO


**steps of integrating some slash commands**

TBD : get example from Vscode runtime.
