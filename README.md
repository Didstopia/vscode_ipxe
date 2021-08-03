# iPXE Syntax Highlighter

iPXE syntax highlighting for Visual Studio Code, based originally on [wwj402's](https://github.com/wwj402) [iPXE syntax highlighter](https://github.com/wwj402/vscode_ipxe).

This extension adds syntax highlighting for both [iPXE](https://ipxe.org/) scripts and [Shoelaces](https://github.com/thousandeyes/shoelaces) template files.

## Features

#### Available

- [x] Basic syntax highlighting for `.ipxe` iPXE scripts

#### Planned

- [ ] Automatically detect `#!ipxe` in scripts to trigger language detection, instead of relying on file extension (`.ipxe`)
- [ ] Add support for [Shoelaces templates](https://github.com/thousandeyes/shoelaces) (`.slc`)
  - [ ] Shoelaces templates support any kind of file, so ideally support automatic language detection
    - [ ] Extend used/detected languages with Shoelaces template syntax highlighting
  - [ ] Update documentation and package configuration file to signify support for both iPXE and SLC
- [ ] Add live documentation to all supported keywords/attributes (pull directly from [ipxe.org](https://ipxe.org/))
  - [ ] Determine and/or reach out to iPXE developers or website maintainers to get permission to scrape the documentation
  - [ ] Aggressively cache the documentation, but provide mechanisms to allow the cache to be cleared by the user
- [ ] Full support for hover information, auto completion, jump to definition, error checking, formatting, refactoring and folding (see [here](https://code.visualstudio.com/api/language-extensions/overview))
- [ ] Add unit tests to ensure the extension keeps working (see [here](https://code.visualstudio.com/api/working-with-extensions/testing-extension))
- [ ] Publish to the Visual Studio Code Marketplace (see [here](https://code.visualstudio.com/api/working-with-extensions/publishing-extension))

## Requirements

No special requirements.

## Extension Settings

Extension settings are not available or necessary, not yet at least.

## Known Issues

- Language detection only works when manually selected (or when opening a file with a `.ipxe` extension)
- Not all language features are available or properly highlighted (eg. variables for example)

## Release Notes

### 0.0.1

Initial release.

## Development

Install `vsce`:
```sh
npm install -g vsce
```

Generate a `.vsix` file:
```sh
vsce package
```

Install the extension to VSCode:
```sh
code --install-extension ipxe-0.0.1.vsix
```

## License

See [LICENSE](LICENSE).

Based on [wwj402's](https://github.com/wwj402) [iPXE syntax highlighter](https://github.com/wwj402/vscode_ipxe).
