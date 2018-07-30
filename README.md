# Sublime Text 3 Settings

### Install Package Control

Step 1: Press Ctrl + ` or View/Show Console

Step 2: Insert code
```
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

### Packages

- Agila Theme
- Emmet
- Erb Snippets
- Ruby on Rails snippets

### Settings

`Preferences/Settings`

```
{
	"auto_complete": true,
	"auto_complete_commit_on_tab": true,
	"copy_with_empty_selection": true,
	"ensure_newline_at_eof_on_save": true,
	"font_size": 13,
	"ignored_packages":
	[
		"Vintage"
	],
	"index_files": true,
	"rulers":
	[
		80
	],
	"tab_size": 2,
	"theme": "Agila Dracula.sublime-theme",
	"translate_tabs_to_spaces": true,
	"trim_trailing_white_space_on_save": true
}
```

### Auto complete settings

`Preferences/Key Bindings`

```
[
  {
    "keys": ["enter"], "command": "commit_completion", "context": [
      { "key": "auto_complete_visible" }
    ]
  },
  {
    "keys": ["tab"], "command": "commit_completion", "context": [
      { "key": "auto_complete_visible" }
    ]
  },
]
```
