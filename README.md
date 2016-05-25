[ESLint-Formatter](https://github.com/TheSavior/ESLint-Formatter) for Sublime Text 3
=================

Sublime Text 3 Plugin to autoformat your javascript code according to the ESLint configuration files you already have.


## Installation

### Linter installation
ESLint (with autoformatting) must be installed on your system before this plugin will work. To install `eslint`, follow the getting started guide: http://eslint.org/docs/user-guide/getting-started.

### Plugin installation

Please use [Package Control](https://sublime.wbond.net/installation) to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can modify the source code, you probably know what you are doing so we won’t cover that here.

To install via Package Control, do the following:

1. Within Sublime Text, bring up the [Command Palette](http://docs.sublimetext.info/en/sublime-text-3/extensibility/command_palette.html) and type `install`. Among the commands you should see `Package Control: Install Package`. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.

1. When the plugin list appears, type `eslint format`. Among the entries you should see `ESLint-Formatter`. If that entry is not highlighted, use the keyboard or mouse to select it.


## Commands
**Command palette:**

- ESLintFormatter: Format this file

**Shortcut key:**

* Linux/Windows: [Ctrl + Shift + H]
* Mac: [Cmd + Shift + H]

## Settings

By default, ESLintFormatter will supply the following settings:

```javascript
{
  // The Nodejs installation path
  "node_path": {
    "windows": "node.exe",
    "linux": "/usr/bin/nodejs",
    "osx": "/usr/local/bin/node"
  },

  // The location of the the globally installed eslint package
  "eslint_path": {
    "windows": "%APPDATA%/npm/node_modules/eslint/bin/eslint",
    "linux": "/usr/bin/eslint",
    "osx": "/usr/local/bin/eslint"
  },

  // Specify this path to a ESLint config file to override the default behavior.
  // Passed to ESLint as --config. Read more here:
  http://eslint.org/docs/user-guide/command-line-interface#c---config
  "config_path": "",

  // Automatically format when a file is saved.
  "format_on_save": false,

  // Only attempt to format files with whitelisted extensions on save.
  // Leave empty to disable the check
  "format_on_save_extensions": [
    "js",
    "jsx",
    "es",
    "es6",
    "babel"
  ]
}
```

* Modify any settings within the `Preferences -> Package Settings -> ESLint-Formatter -> Settings - User` file.

**Project-specific settings override**

To override global plugin configuration for a specific project, add a settings object with a `ESLint-Formatter` key in your `.sublime-project`. This file is accessible via `Project -> Edit Project`.

For example:

```
{
  "folders": [
    {
      "path": "."
    }
  ],
  "settings": {
    "ESLint-Formatter": {
      "format_on_save": true
    }
  }
}
```

## Contributing

If you find any bugs feel free to report them [here](https://github.com/TheSavior/ESLint-Formatter/issues).

Pull requests are also encouraged.
