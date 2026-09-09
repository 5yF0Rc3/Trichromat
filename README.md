# Trichromat

A painter's color mixer for Adobe Photoshop. Three corner colors are blended
with Kubelka–Munk pigment mixing over a Reuleaux-triangle field, with
OK-space lightness control. Click a color in the field and it becomes the
Photoshop foreground.

Trichromat is two parts that talk over a local connection on your own
computer:

- the **Trichromat app**, a small always-on-top window that floats next to
  the Photoshop canvas, and
- the **Trichromat Bridge** plugin inside Photoshop, a thin panel that relays
  the picked color.

This repository holds the documentation, tutorials and the issue tracker.
The source code is not public.

## Download

Beta builds are distributed directly to testers through a private Gumroad
link, together with a license key. If you are a tester and lost the link,
ask the address you received it from.

The download is one zip per platform, each holding the installer, the
Photoshop plugin and a short `INSTALL.txt`:

| File | For |
| --- | --- |
| `Trichromat-<version>-windows.zip` | Windows 10 / 11 |
| `Trichromat-<version>-macos-apple-silicon.zip` | Macs with M1 or later |
| `Trichromat-<version>-macos-intel.zip` | Intel Macs |

Extract the zip to a folder first; the plugin installer needs a real file
on disk, not one inside a zip preview.

Requirements: Photoshop 26.2 or newer with the Creative Cloud desktop app,
Windows 10/11 or macOS 12 or newer.

## Install

### 1. The app

**Windows.** Run `Trichromat-Setup-<version>.exe`. The beta is not yet
code-signed, so Windows SmartScreen shows "Windows protected your PC". Click
*More info*, then *Run anyway*. The installer asks for the install folder and
creates a Start menu and desktop shortcut.

**macOS.** Open the `.dmg` that matches your Mac (`arm64` for Apple Silicon,
`x64` for Intel) and drag Trichromat to *Applications*. The beta is not yet
notarized, so the first launch is blocked. Open *System Settings → Privacy &
Security*, scroll down to the message about Trichromat and click *Open
Anyway*, then confirm. This is needed once.

Start the app once now. That first run registers the `trichromat://` link the
plugin uses to launch it later.

### 2. The Photoshop plugin

Double-click `Trichromat-Bridge-<version>.ccx`. The Creative Cloud desktop
app installs it and warns that the plugin was not verified by Adobe; confirm.
In Photoshop open *Plugins → Trichromat Bridge*. Keep that panel open while
you work: a green dot means it is connected to the app.

If the app is not running, the panel's *Open Trichromat* button starts it.
Photoshop asks for permission the first time.

### 3. Activate

On the first start the app asks for your license key. It is in the Gumroad
receipt e-mail and in your Gumroad library. Copy the key, click *Paste* in
the app, then *Activate*. The mixer window never takes the keyboard away
from Photoshop, which is why the key is pasted with a click rather than
typed. Activation needs an internet connection once; afterwards the app
re-checks the key in the background from time to time.

## Use

In the mixer: **click or drag** in the field moves the selector, **release**
sets the Photoshop foreground, **Alt + release** sets the background. A
corner chip's swatch loads the current Photoshop foreground into that corner.
The lightness row below the field shifts the picked color lighter or darker.
The bottom bar switches between the mix, settings and connection pages.

## Updates

The app checks for a new version on start and shows it on the settings page.
Download the new build from your Gumroad library and run the installer over
the old one. The plugin only needs reinstalling when its version changed;
the release notes say so.

## Reporting problems

Open an issue in this repository and use the bug report template. Please
include the app version (settings page), your OS, the Photoshop version, and
what you did before it went wrong. Screenshots of the connection page help.

## Privacy

The app sends your license key to Gumroad to verify it and downloads a small
version file from this repository to check for updates. Nothing else leaves
your computer. See [PRIVACY.md](PRIVACY.md).

## License

Trichromat is proprietary software licensed under the [EULA](EULA.md). Adobe
and Photoshop are trademarks of Adobe Inc.; Trichromat is an independent
product and is not affiliated with Adobe.
