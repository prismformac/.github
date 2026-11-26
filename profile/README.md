<p align="center">
  <img src="prism-icon.png" width="128" height="128" alt="Prism icon">
</p>

<h1 align="center">Prism</h1>

<p align="center">
  A native, keyboard-first launcher for macOS.<br>
  Apps, files, clipboard history, snippets, windows, and AI, one keystroke away.
</p>

<p align="center">
  <a href="https://prismformac.com"><b>Website</b></a> ·
  <a href="https://download.prismformac.com/Prism.dmg"><b>Download</b></a> ·
  <a href="https://github.com/prismformac/prism-extensions"><b>Extensions</b></a> ·
  <a href="https://github.com/prismformac/prism-extension-kit"><b>Extension Kit</b></a>
</p>

---

## Install

Download [Prism.dmg](https://download.prismformac.com/Prism.dmg), or use Homebrew:

```sh
brew trust --cask natsustan/tap/prism-app
brew install --cask natsustan/tap/prism-app
```

Prism runs on Apple silicon Macs with macOS 26 or later, in English, Simplified Chinese, and Traditional Chinese.

## Build an extension

Extensions add commands, lists, widgets, and preferences to Prism. Each one runs in its own process and answers Prism over stdio, so Prism draws every view and keeps the launcher responsive. Write one as a shell script with no build step, or in Swift with PrismExtensionKit.

1. Copy [`templates/swift`](https://github.com/prismformac/prism-extensions/tree/main/templates/swift) into `extensions/<your-github-name>.<name>`.
2. In Prism, open **Settings › Extensions › Gallery › Import Extension…** and choose the folder. Prism reloads it whenever you rebuild.
3. Test it with `PrismTestHost`, which plays Prism in memory, then check it with `bash tools/check.sh`.
4. Open a pull request. Once it is merged, the release pipeline builds, signs, and publishes it to the Extension Gallery for you.

The [Kit README](https://github.com/prismformac/prism-extension-kit#readme) is the protocol reference.

## Repositories

| Repository | What it holds |
| --- | --- |
| [prism-extensions](https://github.com/prismformac/prism-extensions) | Every extension in the Gallery, with templates, examples, and the release pipeline |
| [prism-extension-kit](https://github.com/prismformac/prism-extension-kit) | The Swift package extensions build against, and the protocol reference |

## In the Gallery

1Password · Agent Usage · Antigravity · Apple Notes · Bear · Caffeinate · Chinese Numbers · Color Picker · GitHub · Kill Process · Lorem Ipsum · Port Manager · Reminders · Screen Sharing · Shottr · Xcode · Zed

…and yours next.
