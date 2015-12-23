# html-convention
## Linter
We use [Html Hint](https://github.com/yaniswang/HTMLHint)
### Installation
1. Install [Node.js](http://nodejs.org) (and [npm](https://github.com/joyent/node/wiki/Installing-Node.js-via-package-manager) on Linux).
1. Install htmlhint globally
  ```
  npm install htmlhint -g
  ```

### Editor configuration
#### Sublime text

1. Install [Sublime Linter](http://www.sublimelinter.com/) using [Package Control](pc)

1. Please use Package Control to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can     modify the source code, you probably know what you are doing so we won’t cover that here.

  To install via Package Control, do the following:

  3. Within Sublime Text, bring up the Command Palette and type install. Among the commands you should see Package Control: Install Package. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.
  3. When the plugin list appears, type htmlhint. Among the entries you should see SublimeLinter-contrib-htmlhint. If that entry is not highlighted, use the keyboard or mouse to select it.


1. @todo: use this repo .htmlhintrc

[pc]: https://sublime.wbond.net/installation

### Disabling rules in your files
Depending on the context of a specific file you might need to exeptionnalu disable one rule.
You can do this using a specific comment syntax :

**Disable a rule:**
```
<!-- htmlhint inline-style-disabled:false -->
```

**Disable multiple rules:**
```
<!-- htmlhint doctype-first:false, attr-value-double-quotes:false, attr-value-not-empty:true -->
```
Any html after those comment will not be checked for the specified rule.
You may enable a rule using the the same syntax but using `rule:true` instead of `rule:false`
