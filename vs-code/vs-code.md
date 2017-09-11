# VS Code

## General Usage

### Download

Download VSCode from [code.visualstudio.com](https://code.visualstudio.com/)

### Installing extensions

![VSCode window with extensions](http://i.imgur.com/9ViTwtb.png)

You may have to restart VSCode when installing extensions

### Opening a project

After cloning a project to a directory, you should open that directory in VS Code.

![VSCode window](http://i.imgur.com/kfXrGyp.png)

### Status bar

The status bar is the bar at the bottom of the window. It contains information such as current Git branch, errors and warnings, file location, line position, and more.

### Git Integration

Excellent integration for entire Git workflow.

#### Diffs

Click Git icon in the sidebar then select the file to diff.

![Git icon](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/b5aa1252019f06e38903d47fabc43552fe8c6f93/media/git_icon.png)

##### Side by side

Default is side by side diff

![side by side view](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/git_side_by_side.png)

##### Inline view

Toggle inline view by clicking more button in the top right.

![inline view icon](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/more_button.png)

![inline view](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/git_inline.png)

#### Branches

Easily switch between branches via the status bar.

![branches gif](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/switch_branches.gif)

#### Staging

##### Stage all

Hover over the number of files and click the plus button.

![stage all gif](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/git_stage_all.gif)

##### Stage selected

Stage a portion of a file by selecting that file (using the arrows) and then staging "selected lines" via the more button.

![stage selected gif](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/git_stage_selected.gif)

#### Undo last commit

![undo last commit](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/master/media/undo_last_commit.gif)

#### See git output

Sometimes I want to see what my tool is doing. Visual Studio Code makes it easy to see what git commands are running. This is helpful when learning git or debugging a difficult source control issue.

> Mac: <kbd>shift+cmd+u</kbd>

> Windows / Linux: <kbd>ctrl+shift+u</kbd>

to run `toggleOutput`. Select Git in the dropdown.

#### Resolve merge conflicts

During a merge click the git icon and make changes in the diff view.

![Git icon](https://raw.githubusercontent.com/Microsoft/vscode-tips-and-tricks/b5aa1252019f06e38903d47fabc43552fe8c6f93/media/git_icon.png)

[More tips and tricks](https://github.com/Microsoft/vscode-tips-and-tricks)

## Useful Shortcuts

- `cmd+shift+p` Command menu: this is the menu where you can run "commands" from vs code or from extensions.  Command availability may depend on the type of file you have focussed.
- `cmd+p` Open file: fuzzy find open file from current project.
- `cmd+[1-9]` Select pane corresponding to number.
- `alt+[arrow_up|arrow_down]` Shift line up or down.
- `f2` Rename symbol

### Useful commands

- "Reload Window" For when your linters are misbehaving, or for when you have changed your installed extensions.
- "Open User Settings" To quickly see all default settings and all your current settings.
- "Markdown: Open Preview" Quickly view a live updating render of the current markdown file.

## Useful settings

```js
{
  // Auto indentation is annoying, especially if you use the move line shortcuts
  "editor.autoIndent": false,
  // Show the minimap position always (normally only visible when scrolling)
  "editor.minimap.showSlider": "always",
  // Make suggestions while typing in comments and strings (default is only other)
  "editor.quickSuggestions": {
    "other": true,
    "comments": true,
    "strings": true
  },
  // Show indent guides
  "editor.renderIndentGuides": true,
  // Make wrapped lines more obvious
  "editor.renderWhitespace": "none",
  "editor.wrappingIndent": "none",
  // A visual ruler
  "editor.rulers": [ 80 ],
  // Keep side bar from jumping around so much
  "explorer.autoReveal": false,
  // Extensions are not stable enough for auto updates IMO
  "extensions.autoUpdate": false,
  // Tween scrool position on page up, page down, or other scroll jumps.
  "editor.smoothScrolling": true,
  // Keep command palatte history between uses
  "workbench.commandPalette.preserveInput": true,
  // Keep files open even after they are deleted on disk. Great if you accidentally remove something.
  "workbench.editor.closeOnFileDelete": false
}
```

## Useful Keybindings

```js
{
  // Quick switch windows
  {
    "key": "cmd+r",
    "command": "workbench.action.quickSwitchWindow"
  },
  {
    "key": "cmd+r",
    "command": "workbench.action.quickOpenNavigateNext",
    "when": "inWindowsPicker"
  },
  // Expand select with similar binds to select by word
  {
    "key": "alt+shift+down",
    "command": "editor.action.smartSelect.grow",
    "when": "editorTextFocus"
  },
  {
    "key": "alt+shift+up",
    "command": "editor.action.smartSelect.shrink",
    "when": "editorTextFocus"
  },
  // Make show git shortcut consistent with show file tree
  {
    "key": "cmd+shift+g",
    "command": "workbench.view.scm"
  },
  {
    "key": "ctrl+shift+g",
    "command": "editor.action.previousMatchFindAction",
    "when": "editorFocus"
  },
  // Left right
  {
    "key": "ctrl+left",
    "command": "workbench.action.focusPreviousGroup",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+right",
    "command": "workbench.action.focusNextGroup",
    "when": "editorTextFocus"
  }
}
```


## Useful extensions

### Productivity

- [Active File In StatusBar](https://marketplace.visualstudio.com/items?itemName=RoscoP.ActiveFileInStatusBar)
- [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
- [Color Picker](https://marketplace.visualstudio.com/items?itemName=anseki.vscode-color)
  - Command: "pick color"
- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
- [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)
  - Command: "file"
- [Git History (git log)](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)
  - Command: "git log"
- [Multiple clipboards for VSCode](https://marketplace.visualstudio.com/items?itemName=slevesque.vscode-multiclip)
- [npm Script Runner](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
  - Command: "npm"
- [npm Instellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)
- [Open In Github](https://marketplace.visualstudio.com/items?itemName=sysoev.vscode-open-in-github)
  - Command: "github"
- [other-window](https://marketplace.visualstudio.com/items?itemName=rrudi.other-window)
  - Command: "open new"
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- [Project Manager](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)
  - "project man"
- [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)
  - Command: "rest"
- [TODO Parser](https://marketplace.visualstudio.com/items?itemName=minhthai.vscode-todo-parser)
  - Command: "todo"
- [Trailing Spaces](https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces)
  - Command: "trailing"
- [Version Lens](https://marketplace.visualstudio.com/items?itemName=pflannery.vscode-versionlens)
  - Adds versions inline for your package.json, pretty useful as a reminder to keep up to date on what your dependencies are doing.
- [View Node Package](https://marketplace.visualstudio.com/items?itemName=dkundel.vscode-npm-source)
  - Command: "package source" while cursor is on a require statement
- [Quit Control for VSCode](https://marketplace.visualstudio.com/items?itemName=artdiniz.quitcontrol-vscode)

#### Language: typescript

- [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)
- [TypeScript Hero](https://marketplace.visualstudio.com/items?itemName=rbbit.typescript-hero)
  - Command: "type", "import"
- [Move TS](https://marketplace.visualstudio.com/items?itemName=stringham.move-ts)

#### Language: es6

- [Babel ES6/ES7](https://marketplace.visualstudio.com/items?itemName=dzannotti.vscode-babel-coloring)
  - After you have installed this plugin, open a `.js` file and run command "Change Language Mode", select "Javascript (Babel)".
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

#### Language: Markdown

- [markdownlinter](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
- [Markdown Table Formatter](https://marketplace.visualstudio.com/items?itemName=josa.markdown-table-formatter)

#### Language: Python

- [Python](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python)
  - If you are also using `pyenv`, you may want this global setting: `"python.pythonPath": "/usr/local/var/pyenv/shims/python"`

### Personalization

- [OceanicNext Theme](https://marketplace.visualstudio.com/items?itemName=gerane.Theme-OceanicNext)
- [Theme-RealGithub](https://marketplace.visualstudio.com/items?itemName=NoHomey.theme-realgithub)
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons)
