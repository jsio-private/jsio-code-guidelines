# Customizing a Theme in VS-Code

Before you get started, here are some good resources to look at:

- [Great docs from ms](https://code.visualstudio.com/Docs/customization/themes) about how to customize the colors in vs-code.
- [Sample_Dark.tmTheme](https://github.com/Microsoft/vscode-extension-samples/blob/master/theme-sample/Sample_Dark.tmTheme) to reference when playing with your own theme.

## Find a Theme

- Command (`cmd+shift+p`): "Install Extensions"
- Search for "theme"
- Install one you like


## Duplicating the Theme

- Command: "Open Extensions Folder"
- Look in `.vscode/extensions/` for the package name of the theme you just installed
  - Copy and paste to "coolTheme.creator-custom"
- `code customTheme.creator-custom` to open the custom theme folder in vs-code


## Priming the Custom Theme

- Edit the following files in the following way: "coolTheme" -> "coolTheme-custom"
  - `.vsixmanifest`
  - `package.json`
- Command: "Reload Window"


## Customizing

- Command: "Color Theme"
  - Select your custom color theme
- You can now edit `themes/*.tmTheme` to customize theme theme
  - Command: "Reload Window" to see the changes take effect


## Contributing

If you work on a theme, you really should find the original repository, fork it, and upstream the changes or add your cool fork to the list below.

Just clone your fork in to the `.vscode/extensions` directory, and reload.


## Office themes

_None yet!_

