# Liquid Glass Version of Classic Emacs Icon

| Light | Dark | Clear | Tinted |
|:-----:|:----:|-------|:------:|
| ![Light](Images/Light.png) | ![Dark](Images/Dark.png) | ![Clear](Images/Clear.png) | ![Tinted](Images/Tinted.png) |

## Overview

A liquid Glass version of [Luis Fernandes' classic Emacs icon](https://www.ee.torontomu.ca/~elf/emacs/logo/) from Emacs 21.

## Usage

### Emacs Plus
If you are using the excellent [Emacs Plus](https://github.com/d12frosted/homebrew-emacs-plus) then this icon is already
included, so all you have to do is specify `retro-emacs-logo` as the icon in your `~/.config/emacs-plus/build.yml` and
re-install:

```yaml
icon: retro-emacs-logo
```

```bash
brew reinstall emacs-plus
```

### Other Emacs

Copy the `Assets.car` file from this repository and place it into `Contents/Resources` within your Emacs.app.

Edit `Contents/Info.plist`, and add/update the following to specify the name of the icon within `Assets.car`:

```xml
<key>CFBundleIconName</key>
<string>retro-emacs-logo</string>
```

You may also need to re-sign the app to placate Gatekeeper.
If you don't have a developer certificate, you can attach an "Ad Hoc" signature like this:

```bash
$ codesign --force --deep --sign - /Applications/Emacs.app
```

*Note* that it may take a while for the icon to update, but you can speed this along by clearing the macOS icon cache
and restarting the Dock.
