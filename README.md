<h1 align="center">
 <img height="100px" src="https://raw.githubusercontent.com/SpikeHD/Dorion/main/src-tauri/icons/icon.png" />
 <br />
 Vorion
</h1>
<div align="center">
 <img src="https://img.shields.io/github/actions/workflow/status/SpikeHD/Dorion/build.yml" />
 <img src="https://img.shields.io/github/package-json/v/SpikeHD/Dorion" />
 <img src="https://img.shields.io/github/repo-size/SpikeHD/Dorion" />
</div>
<div align="center">
 <img src="https://img.shields.io/github/commit-activity/m/SpikeHD/Dorion" />
 <img src="https://img.shields.io/github/release-date/SpikeHD/Dorion" />
 <img src="https://img.shields.io/github/stars/SpikeHD/Dorion" />
 <img src="https://img.shields.io/github/downloads/SpikeHD/Dorion/total" />
</div>

<div align="center">
 Vorion is a fork of Dorion meant to integrate its own WebRTC into the app to allow voice support for Linux distros!
 <br />
 https://discord.gg/agQ9mRdHMZ  -  Original Dorion Discord server (There is no Vorion server
</div>

# Download

<table align="center">
  <tr>
    <th>
      <img src="docs/image/debian.png" width="30%" align="center" />
    </th>
  </tr>

  <tr>
    <td width="30%">
      <div align="center">
        <a href="https://github.com/SpikeHD/dorion/releases/download/v6.6.0/Dorion_6.6.0_amd64.deb">x86_64</a>
        <span>|</span>
        <a href="https://github.com/SpikeHD/dorion/releases/download/v6.6.0/Dorion_6.6.0_armhf.deb">ARM v7</a>
        <span>|</span>
        <a href="https://github.com/SpikeHD/dorion/releases/download/v6.6.0/Dorion_6.6.0_arm64.deb">ARM64</a>
      </div>
    </td>
  </tr>
</table>

<details>

<summary>View bleeding-edge builds</summary>

<h1>Bleeding Edge Builds</h1>
<p>These builds are based on the latest GitHub Actions artifacts. They may not work properly, and they probably contain bugs. Use at your own risk!</p>

<table align="center">
  <tr>
    <th>
      <img src="docs/image/windows.png" width="30%" align="center" />
    </th>
    <th>
      <img src="docs/image/apple.png" width="30%" align="center" />
    </th>
    <th>
      <img src="docs/image/debian.png" width="30%" align="center" />
    </th>
  </tr>

  <tr>
    <td width="30%">
      <div align="center">
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-x86_64-pc-windows-msvc-msi.zip">x86_64</a>
        <span>|</span>
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-aarch64-pc-windows-msvc-nsis.zip">ARM</a>
      </div>
    </td>
    <td width="30%">
      <div align="center">
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-x86_64-apple-darwin-dmg.zip">x86_64</a>
        <span>|</span>
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-aarch64-apple-darwin-dmg.zip">ARM</a>
      </div>
    </td>
    <td width="30%">
      <div align="center">
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-x86_64-unknown-linux-gnu-deb.zip">x86_64</a>
        <span>|</span>
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-armv7-unknown-linux-gnueabihf-deb.zip">ARM v7</a>
        <span>|</span>
        <a href="https://nightly.link/SpikeHD/Dorion/workflows/build/main/dorion-aarch64-unknown-linux-gnu-deb.zip">ARM64</a>
      </div>
    </td>
  </tr>
</table>

</details>

> [!TIP]
> You can find portable builds in the [releases](https://github.com/SpikeHD/dorion/releases/latest/) page. You can also [build](#building) Vorion yourself

# Table of Contents

* [Package Repositories](#package-repositories)
* [Features](#features)
  * [Plugins](#plugins)
  * [Themes](#themes)
* [Platform Support](#platform-support)
* [Building](#building)
  * [Prerequisites](#prerequisites)
  * [Steps](#steps)
* [Known Issues](#known-issues)
* [Troubleshooting](#troubleshooting)
  * [Things you Might be Asked to Provide](#things-you-might-be-asked-to-provide)
  * [General](#general)
  * [Linux](#linux)
* [TODO](#todo)
* [Using Plugins, Extensions, and Themes](#using-plugins-extensions-and-themes)
* [Contributing](#contributing)
  * [Contributors](#contributors)
* [Screenshots](#screenshots)

# Package Repositories

I do **not** maintain any instances of the original Dorion nor Vorion in any package repositories myself, however some very kind people maintain some in their own spare time:

* Linux:
  * Arch AUR (Maintained by [Refined7075](https://github.com/DarkCoder28))
    ```sh
    yay -S dorion-bin
    ```
  * NixOS
    ```sh
    nix-shell -p dorion
    ```
    
> [!NOTE]
> Maintaining Vorion in a different package repository that I don't know about? Feel free to [open a PR](https://github.com/SpikeHD/Dorion/pulls) to add it here!

# Features

* [Significantly smaller](https://github.com/SpikeHD/Dorion/assets/25207995/eb603f1f-f633-4913-a25e-1316b495a08a) than the original Discord client, as well as other web-based alternatives
* Theme support
* Global push-to-talk and custom keybinds
* [Shelter](https://github.com/uwu/Shelter) and (optionally) [Vencord](https://github.com/vendicated/vencord)/[Equicord](https://github.com/equicord/equicord) included out of the box
* Full [RPC/game presence](https://github.com/SpikeHD/rsRPC) support included out of the box. Enable it in "Performance & Extras"!
  * This also requires either the [shelteRPC](https://github.com/SpikeHD/shelter-plugins?tab=readme-ov-file#shelterpc) or [arRPC](https://vencord.dev/plugins/WebRichPresence%20(arRPC)) plugins enabled.
* (Hopefully) better low-end system performance.
* ARM support for ALL platforms
* Feature flags for picking and choosing features (when building from source)

## Plugins

Vorion comes with [shelter](https://github.com/uwu/shelter), so that should cover at least some plugin-related needs. You can also enable client mods like [Vencord](https://github.com/vendicated/vencord) inside the Vorion settings page.
If you want to install plugins not available within the Dorion settings page, ensure you are downloading a browser-compatible version.

> [!NOTE]
> Want official support for another client mod? As long as it works on the web, feel free to submit a [feature request](https://github.com/SpikeHD/Dorion/issues/new/choose)!

> [!TIP]
> Unsure what shelter plugins exist out there? There's more than you think, so try searching `shelter plugins` on GitHub, or use the Plugin Browser plugin:
> 
> `https://spikehd.github.io/shelter-plugins/plugin-browser/`

## Themes

Vorion supports all themes, BetterDiscord and others, with a [couple caveats](#known-issues).

[Jump to "Using Plugins and Themes"](#using-plugins-and-themes)

# Platform Support - Original Dorion

<div width="100%" align="center">

| Feature                                        |Linux - in General|
|------------------------------------------------|------------------|
| Basics (logging in, navigation, text/DMs etc.) | ~[^1]            |
| Voice                                          | ✗[^2]            |
| Themes                                         | ✓                |
| Shelter                                        | ✓                |
| Vorion Plugins                                 | ✓                |

</div>

[^1]: Some people report Dorion freezing on Linux, particularly when GIFs are playing. This is, as far as the original Dorion team can tell, it is a bug in WebkitGTK.

[^2]: Support for WebRTC is hidden behind a build-time flag that is not used in almost every distro. This will be available ~~when WebkitGTK ships with WebRTC support, or if you compile your own WebkitGTK.~~ I get around to adding Vorion's own WebRTC.

# Platform Support - Vorion

<div width="100%" align="center">

| Feature                                        | Debian      |
|------------------------------------------------|-------------|
| Basics (logging in, navigation, text/DMs etc.) | ~[^1]       |
| Voice                                          | ✗[^3]       |
| Themes                                         | ✓?          |
| Shelter                                        | ✓?          |
| Vorion Plugins                                 | ✓?          |

</div>

[^3]: Have yet to integrate WebRTC into Vorion.

# Building

## Prerequisites

* [NodeJS](https://nodejs.org)
* [PNPM](https://pnpm.io/)
* [Rust and Cargo](https://www.rust-lang.org/tools/install)
* [Tauri prerequisites](https://v2.tauri.app/start/prerequisites/)
* [`cargo patch-crate`](https://github.com/mokeyish/cargo-patch-crate)

## Steps

1. Clone/download the repository
2. Open a terminal window in the root project folder
3. Install JS dependencies:

    ```sh
    pnpm install
    ```

4. Pull the latest shelter build (this is used as a backup if it cannot be fetched on the fly)

    ```sh
    pnpm shupdate
    ```
5. Apply the patches

    ```sh
    cd src-tauri
    cargo patch-crate
    ```

6. Build the updater

    ```sh
    pnpm build:updater
    ```

7. (Linux-only) Build the WebKitGTK extension
    ```sh
    cd src-tauri/extension_webkit
    cmake .
    cmake --build .
    ```

8. Build!

    ```sh
    # Build Dorion...
    pnpm tauri build

    # ...or to debug/open in dev mode
    pnpm dev
    ```

All built files will be in `src-tauri/target/(release|debug)/`. Installation files (eg. `.deb`) are located in `bundle/`.

# Known Issues (Original Dorion non-Windows)

* (non-Windows) External images (UserBG, Decor, UserPFP, etc.) will not load
* (non-Windows) Fonts/font-faces will not load

# Troubleshooting

## Things you Might be Asked to Provide

If you submit an issue or ask a question in the Discord, it's likely you will be asked for the following, so please provide them if you can:

* Devtools console output (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> <kbd>i</kbd>, then click "Console")
* `latest.log` output
  * Linux: `~/.config/dorion/logs`

## General

### I can't see Vorion Settings!
* Check if `https://raw.githubusercontent.com/` URLs are being blocked by any system-wide adblockers/firewalls
* Check the devtools console to see if there are any relevant errors

### "Oops! Something went wrong."
(or a similar client crash)
* Disable non-vital client mods/plugins/extensions and try again.
* If you cannot get to the settings menu, you can delete the following items:
  * Linux: `~/.config/vorion/webdata` & `~/.config/vorion/config.json`

## Linux
### White/blank/frozen screen
* Run Vorion with either, or both, of the following environment variables:
  ```sh
  WEBKIT_DISABLE_COMPOSITING_MODE=1
  WEBKIT_DISABLE_DMABUF_RENDERER=1
  ```

# TODO - Original Dorion

* [x] Multi-thread CSS processing
* [x] Use resource files from within the binary itself instead of the filesystem
* [x] Desktop notifications
  * [x] AND displaying the number of notifs in the desktop icon
* [x] Webpack stuff
* [x] Global push-to-talk
* [x] Rich presence(?)
  * [x] FULL rich presence
* [x] Custom keybinds
* [ ] Helper API methods and events for plugins
* [x] Backup localized themes
* [x] Localization timeout
* [x] Safemode key (disable themes and plugins)
* [x] New release notifications
* [x] Logging system
* [ ] Move from `device_query` to `rdev` or `inputbot` (supports more keys. May also just attempt to contribute to `device_query`)
* [x] API abstractions

# TODO - Vorion

* [ ] Integrate Vorion with its own WebRTC
* [ ] Update README with more information regarding Vorion instead of Dorion
 * [x] Initial (incomplete) changes of the README
* [ ] Build pre-compiled binaries and put them in releases
* [ ] See if anyone wants to help maintain a repo or PPA for Vorion

# Using Plugins, Extensions, and Themes

> [!TIP]
> See the `examples` directory for examples of plugins, including how to include external code and themes.

Plugins, extensions, and themes are relatively simple to use, the file structure looks like so on Linux:

```
~/.config/vorion/
    ├── plugins/
    |   └── plugin.js
    └── themes/
        └── theme.css
```

so if you download a plugin, extension, or theme, just pop it into the `plugins`/`extensions`/`themes` folder. If you need help finding them, there are buttons in Vorion settings that'll take you where you need!

> [!NOTE]
> Themes can also be installed by clicking `Install Theme from Link` in Theme settings, if you prefer

# Contributing
### Original Dorion
Issues, PRs, etc. are all welcome! For guidelines and tips, see [CONTRIBUTING.md](https://github.com/SpikeHD/Dorion/blob/main/CONTRIBUTING.md)
### Vorion
Help with makign Vorion work across distros is also welcome.
## Contributors

~~<a href="https://github.com/spikehd/dorion/graphs/contributors">~~
  ~~<img src="https://contrib.rocks/image?repo=spikehd/dorion" />~~
</a>

# Screenshots

## Installer Size Comparison (Windows)
<img width="100%" src="https://github.com/SpikeHD/Dorion/assets/25207995/55ce8a69-1732-4e17-90f6-5582bcc21d0c" />

## Full Installed Size Comparison (Windows)
<img width="100%" src="https://github.com/SpikeHD/Dorion/assets/25207995/eb603f1f-f633-4913-a25e-1316b495a08a" />

## Loading screen
<img width="100%" src="https://github.com/SpikeHD/Dorion/assets/25207995/5c9041da-038c-465c-b048-a7c4034a45e0" />

## Settings Menu
<img width="100%" src="https://github.com/SpikeHD/Dorion/assets/25207995/b34577eb-a583-4c9d-abf9-fde791e0f0aa" />

Theme: [Catpuccin - Frappe](https://github.com/catppuccin/discord)

<img width="100%" src="https://github.com/SpikeHD/Dorion/assets/25207995/c73a2333-31fb-404a-9489-5e1b1f8cfa54" />

Theme: [Fluent](https://betterdiscord.app/theme/Fluent)
