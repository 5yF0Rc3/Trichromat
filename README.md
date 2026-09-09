# Trichromat

A painter's color mixer for Adobe Photoshop. Three corner colors are blended
with Kubelka–Munk pigment mixing over a Reuleaux-triangle field, with
OK-space lightness control. Click a color in the field and it becomes the
Photoshop foreground.

Trichromat has two parts:
- the **Trichromat app**, a small always-on-top window that floats next to
  the Photoshop canvas, and
- the **Trichromat Bridge** plugin inside Photoshop that connects to the app.

The app **can be used without Photoshop!** in **Solo**-mode, you can copy the selected Color as HEX to the clipboard.

## Download and Requirement
**Photoshop 26.2.0** or **newer** versions required with the Creative Cloud desktop app. Windows 10/11 or macOS 12 or newer.

[Get it on Gumroad](https://745191790950.gumroad.com/l/trichromat)


## Install

### 1. The app
Extract the zip to a folder.

**Windows.** Windows SmartScreen shows "Windows protected your PC". Click
*More info*, then *Run anyway*. The installer asks for the install folder and
creates a Start menu and desktop shortcut.

**macOS.** Open the `.dmg` that matches your Mac (`arm64` for Apple Silicon,
`x64` for Intel) and drag Trichromat to *Applications*. The app is not yet
notarized, so the first launch is blocked. Open *System Settings → Privacy &
Security*, scroll down to the message about Trichromat and click *Open
Anyway*, then confirm. This is needed once.

The App has to be started once, to be visible for the Photoshop plugin.

### 2. The Photoshop plugin
Double-click `Trichromat-Bridge.ccx`. The Creative Cloud desktop
app installs it and warns that the plugin was not verified by Adobe; confirm.
In Photoshop open *Plugins → Trichromat Bridge*.

If the app is not running, the panel's *Open Trichromat* button starts it.
Photoshop asks for permission the first time.

### 3. Activate

On the first start the app asks for your license key. It is in the Gumroad
receipt e-mail and in your Gumroad library. Copy the key, click *Paste* in
the app, then *Activate*. Activation needs an internet connection once; afterwards the app
re-checks the key in the background from time to time.

### Updates
The app checks for a new version on start and shows it on the settings page.
Download the new build from your [Gumroad library](https://gumroad.com/library) and run the installer over
the old one. 

## Use

In the mixer: **click or drag** in the field moves the selector, **release**
sets the Photoshop foreground, **Alt + release** sets the background. 

... Tutorial follows ...

## Reporting problems or feature ideas

Open an issue in this repository and use the report template. Please
include for a bug the app version (settings page), your OS, the Photoshop version, and
what you did before it went wrong. Screenshots of the connection page help.
You can contact me directly: [trichromat@lukashefti.ch]()

## Privacy

The app sends your license key to Gumroad to verify it and downloads a small
version file from this repository to check for updates. Nothing else leaves
your computer. See [PRIVACY.md](PRIVACY.md).

## License

Trichromat is proprietary software licensed under the [EULA](EULA.md). Adobe
and Photoshop are trademarks of Adobe Inc.; Trichromat is an independent
product and is not affiliated with Adobe.
