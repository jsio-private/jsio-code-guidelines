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

## Useful Shortcuts

- `cmd+shift+p` Command menu: this is the menu where you can run "commands" from vs code or from extensions.  Command availability may depend on the type of file you have focussed.
- `cmd+p` Open file: fuzzy find open file from current project.
- `cmd+[1-9]` Select pane

### Useful commands

- "Reload Window" For when your linters are misbehaving, or for when you have changed your installed extensions.
- "Open User Settings" To quickly see all default settings and all your current settings.

## Useful settings

```js
{
  // A visual ruler
  "editor.rulers": [ 80 ],
  // Make wrapped lines more obvious
  "editor.wrappingIndent": "none",
  "editor.renderWhitespace": "none",
  // Keep side bar from jumping around so much
  "explorer.autoReveal": false,
  // Always include all words from the current document.
  "javascript.suggest.alwaysAllWords": true,
  // Complete functions with their parameter signature.
  "javascript.suggest.useCodeSnippetsOnMethodSuggest": true,
  // Show indent guides
  "editor.renderIndentGuides": true
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

#### Language: typescript
- [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)
- [Types auto installer](https://marketplace.visualstudio.com/items?itemName=jvitor83.types-autoinstaller)
- [TypeScript Hero](https://marketplace.visualstudio.com/items?itemName=rbbit.typescript-hero)
  - Command: "type", "import"

#### Language: es6
- [Babel ES6/ES7](https://marketplace.visualstudio.com/items?itemName=dzannotti.vscode-babel-coloring)
  - After you have installed this plugin, open a `.js` file and run command "Change Language Mode", select "Javascript (Babel)".
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

#### Language: Markdown
- [markdownlinter](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

#### Language: Python
- [Python](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python)

### Personalization
- [OceanicNext Theme](https://marketplace.visualstudio.com/items?itemName=gerane.Theme-OceanicNext)
- [Theme-RealGithub](https://marketplace.visualstudio.com/items?itemName=NoHomey.theme-realgithub)
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=robertohuertasm.vscode-icons)
