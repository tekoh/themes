# Windows Terminal Themes

Preview and copy themes for the new [Windows Terminal (Preview)](https://github.com/microsoft/terminal).

![Preview of the Windows Terminal Themes](https://github.com/atomcorp/themes/raw/master/public/preview.png)

[https://atomcorp.github.io/themes/](https://atomcorp.github.io/themes/)

---

## Info

Most themes are copied from [iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes). So thanks and credit to them and all the theme designers.

## How to use the themes

This app let's you copy a theme you like (or download a json file with all of them). 

The [official docs for Windows Terminal](https://github.com/microsoft/terminal/blob/master/doc/user-docs/UsingJsonSettings.md) seem very thorough explaining how to change the settings. But essentially:
- open Window Preview settings (called profile.json)
- add your chosen theme(s) to `schemes`
- in `profiles`, find the shell you're using (eg cmd, powershell, ubuntu) and replace `colorScheme` with the name of the theme
- celebrate 🥳

## Contribute a theme

Ideally for the ecosystem new themes should be proposed to [iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes), then everyone can benefit. 

If not, new themes can be add added with a pull request, just add them to the list in `src/custom-colour-schemes.json` and compile the list with `yarn themes`.

## Running

Install using `yarn start`. Testing is tbc.

### Compiling the themes 

The json list of themes `src/colour-schemes.json` is generated by running `yarn themes`, it merges all the schemes found in the [iTerm2-Color-Schemes windowsterminal dir](https://github.com/mbadolato/iTerm2-Color-Schemes/tree/master/windowsterminal) using the GitHub API, then combines it with `src/custom-colour-schemes.json` in this repo.

To run `yarn themes`, you also need to include a GitHub personal access token (get it at [https://github.com/settings/tokens](https://github.com/settings/tokens)). You'll then need to add a file in the root dir called `private.json` that looks like: 

```json
{"token": "Your Github Personal access token"}
```

This file is ignored by `.gitignore`, so it won't be shared

## Todo

- a way to share themes
- testing with [cypress](https://www.cypress.io/)
- automating the compilation step

## Notes

- aims are to be simple and accessible
- this project is based around: React (create-react-app), TypeScript, Node, Github Pages, immer and CSS Grid
- the following projects were really useful [clipboard-polyfill](https://github.com/lgarron/clipboard-polyfill), [resize-observer-polyfill](https://github.com/que-etc/resize-observer-polyfill), [file-saver](https://github.com/eligrey/FileSaver.js) and [get-contrast](https://github.com/johno/get-contrast). Thanks!
