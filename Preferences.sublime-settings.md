## Install Package Control

Install [Package Control](https://sublime.wbond.net/installation) for easy package management. 

1. Open the console with `` Ctrl+` ``
2. Paste in the following:

````
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
````

From here on out, use [Package Control](https://sublime.wbond.net/browse) to install **everything**. `⌘`+`Shift`+`P`, then type `Install` to get a list of installable packages you can livesearch through. Watch the Status Bar for installation progress.

## Add Some Style

Install [Soda Theme](http://buymeasoda.github.io/soda-theme/) for some UI customisations. You'll need to restart Sublime after installation for the changes to take effect.

## Add Some Useful Packages

All installed with Package Manager. `⌘`+`Shift`+`P` and type `install`. Then start typing the name of the extension you want to install.

### General 

- [SideBarEnhancements](https://github.com/titoBouzout/SideBarEnhancements/tree/st3) Provides enhancements to the operations on Sidebar of Files and Folders.
- [SublimeCodeIntel](https://sublime.wbond.net/packages/SublimeCodeIntel) - Full-featured code intelligence and smart autocomplete engine.
- [AdvancedNewFile](https://sublime.wbond.net/packages/AdvancedNewFile) - Fast file creation within a project.
- [Nettuts+ Fetch](https://sublime.wbond.net/packages/Nettuts%2B%20Fetch) - Fetch the latest version of remote files and zip packages.
- [Gist](https://sublime.wbond.net/packages/Gist) - Gist management.Create, read, update, and delete gists from within Sublime. 
- [ApplySyntax](Provides a real-time Word Count and character count in the status-bar) - Better syntax detection.
- [Alignment](https://sublime.wbond.net/packages/Alignment) - Easy alignment of multiple selections and multi-line selections.
- [DocBlockr](https://sublime.wbond.net/packages/DocBlockr) - Simplifies writing DocBlock comments in Javascript, PHP, CoffeeScript, Actionscript, C & C++.

### HTML, CSS & JS
- [Emmet](https://sublime.wbond.net/packages/Emmet) - (Formerly Zen Coding) For lightning fast coding.
- [SublimeLinter](https://github.com/SublimeLinter/SublimeLinter3#sublimelinter3) - Coming soon. Code linting & hinting for HTML/CSS/JS.
- [Sass](https://sublime.wbond.net/packages/Sass) - Adds syntax highlighting and tab/code completion for Sass and SCSS files. Also features Emmet shortcuts for many CSS properties.

### Git
- [GitGutter](https://github.com/jisaacks/GitGutter) tracks line changes in the gutter.
- [Modific](https://sublime.wbond.net/packages/Modific) - Highlight lines changed since the last commit.

### Markdown
- [MarkdownEditing](https://sublime.wbond.net/packages/MarkdownEditing) - Better Markdown editing from within Sublime.
- [Markdown Preview](https://sublime.wbond.net/packages/Markdown%20Preview) - Preview and build your markdown files quickly in your web browser from sublime text 2/3.
- [SmartMarkdown](https://sublime.wbond.net/packages/SmartMarkdown) - Some useful shortcuts for working with Markdown in Sublime. Brings better integration with Pandoc.
- [WordCount](https://sublime.wbond.net/packages/WordCount) - Provides a real-time Word Count and character count in the status-bar.

### Laravel 

- [Laravel 4 Facades](https://sublime.wbond.net/packages/Laravel%204%20Facades) - Easy access to the Laravel 4 Facades.

### ExpressionEngine

- [ExpressionEngine Add-on Builder](https://sublime.wbond.net/packages/ExpressionEngine%20Add-On%20Builder) - *(Waiting on ST3 support)* - Quick scaffold for EE addon development.

### Apache Conf

- [ApacheConf](https://sublime.wbond.net/packages/ApacheConf.tmLanguage) - For editing .htaccess and .conf files.

## Add Some Colour

- [Dayle Rees Color Schemes](https://github.com/daylerees/colour-schemes) - A collection of high quality colour schemes.
- [Github Color Theme](https://sublime.wbond.net/packages/Github%20Color%20Theme) - Simple github colour scheme.
- [Solarized Toggle](https://sublime.wbond.net/packages/Solarized%20Toggle) - A very simple plugin that lets you toggle between the dark and light default Solarized colour schemes.

## Settings - User

Accessible via: `SublimeText` &rarr; `Preferences` &rarr; `Settings – User`, or with `⌘`+`,'.'

This is a JSON file of custom user configuration settings. Kept in alphabetical order for easy reference.
This setting is inspired by [ijy's setting](https://gist.github.com/ijy/7399688) and adjusted by the setting of [TaylorOtwell](https://medium.com/@taylorotwell/how-i-work-a22010d1ad82).

**Note:** *As a JSON file no comments can be included. Any you add will be stripped out on saving.*
```
{
	"auto_complete": true,
	"auto_complete_commit_on_tab": true,
	"auto_complete_with_fields": true,
	"bold_folder_labels": false,
	"caret_style": "phase",
	"color_scheme": "Packages/Color Scheme - Default/Blackboard.tmTheme",
	"default_encoding": "UTF-8",
	"detect_indentation": true,
	"ensure_newline_at_eof_on_save": true,
	"folder_exclude_patterns":
	[
		".git",
		".bundle",
		".sass-cache"
	],
	"font_face": "Menlo",
	"font_options":
	[
		"subpixel_antialias"
	],
	"font_size": 12.0,
	"highlight_line": true,
	"highlight_modified_tabs": true,
	"ignored_packages":
	[
		"Vintage"
	],
	"line_numbers": true,
	"line_padding_bottom": 5,
	"line_padding_top": 5,
	"phpunit-sublime-terminal": "iTerm",
	"soda_classic_tabs": true,
	"soda_folder_icons": false,
	"tab_size": 4,
	"theme": "Soda Dark.sublime-theme",
	"translate_tabs_to_spaces": true,
	"trim_trailing_white_space_on_save": true,
	"word_wrap": true
}
```
## Key Bindings - User

Accessible via: `SublimeText` &rarr; `Preferences` &rarr; `Key Bindings – User`. 

Key bindings are the productivity engine which allow you to become one with your text editor. I try to stick with all the defaults to make for an easy install and less chance of potential future clashes. The following are a few small edits I make along with some package specific controls:

```
[
    // Reveal the currently open file in the sidebar
    { "keys": ["ctrl+super+r"], "command": "reveal_in_side_bar" },

    // AdvancedNewFile
    { "keys": ["ctrl+alt+n"], "command": "advanced_new_file_new" },

    // Create a new snippet [Jeffrey Way]
    { "keys": ["alt+super+n"], "command": "new_snippet" },

    // Open iTerm
    { "keys": ["ctrl+alt+t"], "command": "open_terminal" },

    // Select (or type) the syntax to apply to the current view.
    { "keys": ["ctrl+shift+y"], "command": "show_overlay", "args": {"overlay": "command_palette", "text": "Set Syntax: "} },

    // swap the keybindings for paste and paste_and_indent
    { "keys": ["super+v"], "command": "paste_and_indent" },
    { "keys": ["super+shift+v"], "command": "paste" },

    // [HTMLPrettify] Format your HTML, CSS, and JS
    { "keys": ["super+shift+h"], "command": "htmlprettify" },

    // Close tag
    { "keys": ["super+."], "command": "close_tag" },

    // Alignment
    { "keys": ["super+shift+a"], "command": "alignment" },

    // Wrap selection in tag
    {
        "keys"      :   ["alt+shift+t"],
        "command"   :   "insert_snippet",
        "args": {
            "contents": "<${1:p}>${0:$SELECTION}</${1}>"
        }
    },

]
```
