# iPXE Syntax Highlighter

iPXE syntax highlighting for Visual Studio Code, based originally on [wwj402's](https://github.com/wwj402) [iPXE syntax highlighter](https://github.com/wwj402/vscode_ipxe).

This extension adds syntax highlighting for both [iPXE](https://ipxe.org/) scripts and [Shoelaces](https://github.com/thousandeyes/shoelaces) template files.

## Usage

As the extension is not yet available on the official marketplace, it can only be installed manually.

Browse to the latest GitHub Actions builds, where you will find the latest version is a build artifact, then simply download it and install it either through the Visual Studio Code IDE, or manually by running the following command:

```sh
# Replace the version number etc. where appropriate
code --install-extension ipxe-syntax-highlighter-0.0.1.vsix
```

## Features

### Available Now

- [x] Basic syntax highlighting for `.ipxe` iPXE scripts

### In Progress

- [ ] Fix multiple/combined languages not working with `.slc` [Shoelaces templates](https://github.com/thousandeyes/shoelaces)
  - [ ] Fix `test.ipxe.slc` (iPXE format not detected/applied, only Shoelaces format is being applied)
  - [ ] Fix `test.json.slc` (JSON format not detected/applied, only Shoelaces format is being applied)
  - [ ] Fix `test.yaml.slc` (YAML format not detected/applied, only Shoelaces format is being applied)
- [ ] Add basic support for [Shoelaces templates](https://github.com/thousandeyes/shoelaces) (`.slc`)
  - [ ] Add support for `{{define "foo.ext" -}}` and `{{end}}` keywords

### Planned Next

- [ ] Automatically detect `#!ipxe` in scripts to trigger language detection, instead of relying on file extension (`.ipxe`)
- [ ] Add more support for [Shoelaces templates](https://github.com/thousandeyes/shoelaces) (`.slc`)
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
code --install-extension ipxe-syntax-highlighter-0.0.1.vsix
```

## License

See [LICENSE](LICENSE).

Based on [wwj402's](https://github.com/wwj402) [iPXE syntax highlighter](https://github.com/wwj402/vscode_ipxe).
