<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-31-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

![](./docs/img/new_logo.png)

[![Build Status](https://travis-ci.com/hackjutsu/Lepton.svg?branch=master)](https://travis-ci.com/hackjutsu/Lepton)
[![Dependency Status](https://david-dm.org/hackjutsu/Lepton.svg?style=flat-square)](https://david-dm.org/hackjutsu/Lepton)
[![MIT Licensed](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://opensource.org/licenses/MIT)
[![lepton](https://snapcraft.io/lepton/badge.svg)](https://snapcraft.io/lepton)

**Lepton** is a lean code snippet manager powered by GitHub Gist. [Check out the latest release.](https://github.com/hackjutsu/Lepton/releases)

## Features
- Unlimited public/secret snippets
- Unlimited tags
- Language groups
- Markdown/JupyterNotebook
- [GitHub Enterprise](https://github.com/hackjutsu/Lepton/wiki/FAQ#enable-github-enterprise)
- GitHub token
- Immersive mode
- [Customizable](https://github.com/hackjutsu/Lepton/wiki/Configuration)
- Light/Dark theme
- macOS/Win/Linux
- Dashboard
- [Search](https://github.com/hackjutsu/Lepton/wiki/FAQ#search)
- [Proxy](https://github.com/hackjutsu/Lepton/wiki/FAQ#proxy)
- Free

![Screenshot](./docs/img/portfolio/stay_organized.png)

| [Light Theme](https://github.com/hackjutsu/Lepton#customization)     | [Dark Theme](https://github.com/hackjutsu/Lepton#customization)    |
| :-------------:| :-----:|
|![Screenshot](./docs/img/portfolio/lepton-light.png)|![Screenshot](./docs/img/portfolio/lepton-dark.png)|

|      Organize         |  Markdown | Jupyter Notebook |
| :-------------:| :-----:| :-----: |
| ![Screenshot](./docs/img/portfolio/stay_organized.png) | ![Screenshot](./docs/img/portfolio/markdown.png) | ![Screenshot](./docs/img/portfolio/jupyterNotebook.png) |

|      Search (*⇧ + Space*)         |    Immersive Mode *(⌘/Ctrl + i)*    | Dashboard *(⌘/Ctrl + d)* |
| :-------------:| :-----:| :-----: |
| ![Screenshot](./docs/img/portfolio/search_bar.png) | ![Screenshot](./docs/img/portfolio/immersive.png) | ![Screenshot](./docs/img/portfolio/dashboard.png)


## Shortcuts
| Function       | Shortcut       |  Note     |
| :------------: |:-------------: |:-----:|
| New Snippet    | `Cmd/Ctrl + N` | Create a snippet      |
| Edit Snippet   | `Cmd/Ctrl + E` | Edit a snippet      |
| Delete Snippet   | `Cmd/Ctrl + Del` | Delete selected snippet      |
| Submit         | `Cmd/Ctrl + S` | Submit the changes from the editor      |
| Cancel         | `Cmd/Ctrl + ESC` | Exit the editor without saving   |
| Sync           | `Cmd/Ctrl + R` | Sync with remote Gist server   |
| Immersive Mode | `Cmd/Ctrl + I` |  Toggle the [Immersive mode](https://github.com/hackjutsu/Lepton/blob/master/docs/img/portfolio/immersive.png)    |
| Dashboard      | `Cmd/Ctrl + D` |  Toggle the [dashboard](https://github.com/hackjutsu/Lepton/blob/master/docs/img/portfolio/dashboard.png)     |
| About Page     | `Cmd/Ctrl + ,` |  Toggle the [About page](https://github.com/hackjutsu/Lepton/blob/dev/docs/img/portfolio/about.png)    |
| Search         | `Shift + Space`|  Toggle the [search bar](https://github.com/hackjutsu/Lepton/blob/master/docs/img/portfolio/search_bar.png)    |

## Customization
Lepton's can be customized by `<home_dir>/.leptonrc`! You can find its exact path in the About page by `Command/Ctrl + ,`. Create the file if it does not exist.

- Theme (light/dark)
- Snippet
- Editor
- Logger
- Proxy
- Shortcuts
- Enterprise
- Notifications

Check out the [configuration docs](https://github.com/hackjutsu/Lepton/wiki/Configuration) to explore different customization options.

## Tech Stack
![Based on](./docs/img/erb-logo.png)

1. Framework: [Electron](http://electron.atom.io/)
2. Bundler: [Webpack](http://webpack.github.io/docs/), [Babel](https://babeljs.io), [electron-builder](https://github.com/electron-userland/electron-builder)
3. Language: [ES6](https://babeljs.io/docs/learn-es2015/), [Sass](http://sass-lang.com/)
4. Library: [React](https://facebook.github.io/react/), [Redux](https://github.com/reactjs/redux), [Redux Thunk](https://github.com/gaearon/redux-thunk), [Redux Form](http://redux-form.com/)
5. Lint: [ESLint](http://eslint.org/)

## Installation
- macOS/Windows/Linux: Download [the released packages](https://github.com/hackjutsu/Lepton/releases)
- macOS: Install via Homebrew
```bash
brew install --cask lepton
```
- Linux: Install via [Snap Store](https://snapcraft.io/lepton)
```bash
snap install lepton
```
![Based on](./docs/img/lepton-ubuntu-tweet2.png)

## Development


### Install dependencies

```bash
$ git clone https://github.com/hackjutsu/Lepton.git
$ cd Lepton && yarn install
```

```bash
# inspect stale dependencies
$ yarn check-outdated
```

### Client ID/Secret
[Register your application](https://github.com/settings/applications/new), and put your client id and client secret in `./configs/account.js`.
```js
module.exports = {
  client_id: <your_client_id>,
  client_secret: <your_client_secret>
}
```

### Run
```bash
$ yarn build && yarn start
```

## Build Installer App
>Read [electron-builder docs](https://github.com/electron-userland/electron-builder#readme) and check out the [code signing wiki](https://github.com/electron-userland/electron-builder#code-signing) before building the installer app.

Build apps for macOS.
```bash
$ yarn dist -m
```
Build apps for Windows.
```bash
$ yarn dist -w
```
Build apps for Linux.

>Need a running [Docker](https://www.docker.com/) daemon to build a `snap` package.
```bash
$ yarn dist -l
```
Build apps for macOS, Windows and Linux.
```bash
$ yarn dist -wml
```
Build apps for the current OS with the current arch.
```bash
$ yarn dist
```

## FAQ
[--> Wiki FAQ](https://github.com/hackjutsu/Lepton/wiki/FAQ)
