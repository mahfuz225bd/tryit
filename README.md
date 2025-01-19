# trycode

This is a unofficial desktop version of w3school trycode editor developed for practicing html coding. I have plan for adding more features like file system or others with other programming facilities.

Firstly, install all dependencies with:

```bash
npm install
```

Then, run with command:

```bash
npm run tauri dev
```

To build:

```bash
npm run tauri build
```

But, before running the build command, make sure that your PC has Rust and Cargo installed. To check if Rust and Cargo are installed, run the command:

```bash
rustc --version
cargo --version
```

You should see output similar to:

```
rustc 1.65.0 (897e37553 2022-11-02)
cargo 1.65.0 (0a5e40e37 2022-11-02)
```

If output is not displayed, Rust and Cargo is not installed on your computer; you need install it. For installation, follow to the [rust installation](https://www.rust-lang.org/tools/install) notes. A binary file in `src-tauri/target/release` will be generated once building is accomplished.

## File/Folder Structure

To introduce the necessary files and folders that will support future updates of the app, as outlined below in a structured format:

```
trycode/
├── binaries/                        # Contains the binary files generated after building
│   ├── trycode_WIN_x64.exe            # The built executable file for 64-bit Windows
│   ├── trycode_MacOS_x64.exe          # The built executable file for 64-bit MacOS
├── src/                             # Main source code of the application
│   ├── .vscode/                     # Contains project-specific settings and configurations for Visual Studio Code, including preferences, tasks, and debug configurations.
│   ├── assets/                      # Contains assets like CSS and icons used in the application
│   │   ├── css/                     # Folder for CSS files
│   │   │   ├── btn.css              # Styles for buttons
│   │   │   ├── icon-bar.css         # Styles for the icon bar
│   │   │   ├── default.css          # Default styles for the app (btn.css and icon-bar.css are already imported)
│   │   ├── icons/                   # Folder for icon files
│   ├── index.html                   # The main HTML file for the app
│   ├── main.js                      # Main JavaScript file for app functionality
│   ├── styles.css                   # General styles for the application
├── src-tauri/                       # Contains the Tauri-specific source and configuration files
│   ├── icons/                       # Tauri-specific icons
│   ├── .gitignore                   # Git ignore file for the Tauri source directory (generated by Cargo)
│   ├── target/                      # Directory where the Tauri build output is stored
│   ├── Cargo.toml                   # Rust dependencies and configuration for Tauri
│   ├── tauri.conf.json              # Configuration file for Tauri build and settings
├── .gitignore                       # Global git ignore file for the entire project
├── package.json                     # Contains project metadata and dependencies for the JavaScript app

```

## Features for Future Releases

Here are some features that I plan to include for the future releases:

- Tab action on code input

- Colorful syntax highlighting

- Toggling auto run (with saving toggled value is true or false into localStorage to remain same after closing the editor)

- Dynamic resizing of the code input and output is allowed with a drag-bar (where code input + output should equal 100%)

- Console for JS code

- Along with only HTML, HTML-CSS-JS like codepen.io

  - Downloading whole project
  - Saving the whole project as a project file

- Allow adding multiple files with a tree-structured view of files/folders.

  - Tab for the switching

- Drag and drop to open a file to edit

- Allow open with this code editor though context menu of the file explorer

- Build-in bash command prompt

- Built-in git

- Allow coding for other platforms like Node.js, PHP, Python, Java, C, C++, and others with allowing instant clickable downloads and installations of compilers and interpreters of different versions and authors.

- Zoom in/out for code and output

- Find/Replace

- Allowing to add current date/time with F5 or others

- Menubar

- Status bar

  - Line, Col
  - Character Counts
  - Zoom values of code and output

- Settings

  - Toggle on/off syntax highlighting
  - Managing versions and variants (authors) of the platforms

- Allowing to open and publish of a project of a git repository

- Web publishing

  - Free or limited free publishing with a subdomain
  - Free publishing as a GitHub page
  - Publishing directly like FileZilla which should be as easy as possible

- Optional login/logout for well managing

## TODOs Before Releasing the Next Version

- Revise whole code of this editor and re-write optimized version

- Remove title text for both textarea and iframe

- Try to add more features as possible, which should be at least for HTML or HTML-CSS-JS
