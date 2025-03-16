# TypeSpec

## Generating sublime-syntax (for bat)

1. Download tmLanguage JSON and convert to plist format:

```sh
	curl -sS https://raw.githubusercontent.com/microsoft/typespec/main/grammars/typespec.json \
	| plutil -convert xml1 -o typespec.tmLanguage -
```

2. Convert to sublime-syntax format ([credit](https://forum.sublimetext.com/t/trying-to-convert-tmlanguage-syntax-to-sublime-syntax/53427)) 
	1. Download Sublime Text 🥴
	2. Open `typespec.tmLanguage`
	3. _Tools > Developer > New Syntax from typespec.tmLanguage_
	4. Save as `typespec.sublime-syntax`
