# TypeSpec

## Generating sublime-syntax (for bat)

1. Download tmLanguage JSON and convert to plist format:

```sh
curl -sS https://raw.githubusercontent.com/microsoft/typespec/main/grammars/typespec.json \
| plutil -convert xml1 -o typespec.tmLanguage -
```

2. Convert to sublime-syntax format

```sh
nix run nixpkgs#sublime_syntax_convertor typespec.tmLanguage
```
