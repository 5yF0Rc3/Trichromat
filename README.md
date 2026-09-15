# Trichromat

A painter's color mixer for Adobe Photoshop and Krita. Three corner colors are blended
with Kubelka–Munk pigment mixing over a Reuleaux-triangle field, with OK-space lightness control. Click a color in the field and it becomes the foreground color in your painting app.

Trichromat has two parts:
- the **Trichromat app**, a small always-on-top window that floats next to
  your canvas, and
- the **Trichromat Bridge** plugin inside Photoshop or Krita that connects to the app.

The app **can be used on its own!** in **Solo**-mode, you can copy the selected Color as HEX to the clipboard.

## Download and Requirement
**OS:** <ins>Windows 10/11</ins> or <ins>macOS 12</ins> or newer.

**For Photoshop:** <ins>Photoshop 26.2.0</ins> or newer versions required with the <ins>Creative Cloud</ins> desktop app. 

**For Krita:** <ins>Krita 5.2</ins> or newer. Tested on 5.3 and 6.0.

**Download:** [Get it on Gumroad](https://745191790950.gumroad.com/l/trichromat)


## Install
### 1. The app
Extract the zip to a folder.

#### Windows
Windows SmartScreen shows "Windows protected your PC". Click *More info*, then *Run anyway*. The installer asks for the install folder and creates a Start menu and desktop shortcut.

#### MacOS
Open the `.dmg` that matches your Mac (`arm64` for Apple Silicon, `x64` for Intel) and drag Trichromat to *Applications*. 

> [!IMPORTANT]
> The app is not yet notarized, so the first launch is blocked. Open *System Settings → Privacy & Security*, scroll down to the message about Trichromat and click *Open Anyway*, then confirm. This is needed once.
> 
> <img width="300" alt="apple 2" src="/images/apple 2.png" />


### 2. The plugin
The App has to be started once, to be visible for the plugin. Install the
plugin for the app you paint in — both, if you use both.

#### Photoshop
Double-click `Trichromat-Bridge.ccx`. The Creative Cloud desktop app installs it and warns that the plugin was not verified by Adobe; **confirm**.
In Photoshop open *Plugins → Trichromat Bridge*.

If the app is not running, the panel's *Open Trichromat* button starts it.
Photoshop asks for permission the first time.

#### Krita
In Krita choose *Tools → Scripts → Import Python Plugin from File…* and pick
`Trichromat-Krita-<version>.zip` from the download. Restart Krita.

Open *Settings → Configure Krita → Python Plugin Manager*, tick **Trichromat
Bridge** if it is not ticked already, and restart Krita once more.

*Settings → Dockers → Trichromat Bridge* opens a small docker with the
connection status and an *Open Trichromat* button. The connection works
without the docker open.

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
sets the foreground color in Photoshop or Krita, **Alt + release** (Option on
macOS) sets the background. 

... Tutorial follows ...

## Reporting problems or feature ideas

Open an issue in this repository and use the report template. Please
include for a bug the app version (settings page), your OS, your Photoshop or
Krita version, and what you did before it went wrong. Screenshots of the connection page help.
You can contact me directly: [trichromat@lukashefti.ch]()

## Privacy

The app sends your license key to Gumroad to verify it and downloads a small
version file from this repository to check for updates. Nothing else leaves
your computer. See [PRIVACY.md](PRIVACY.md).

## License

Trichromat is proprietary software licensed under the [EULA](EULA.md). Adobe
and Photoshop are trademarks of Adobe Inc.; Krita is a trademark of the Krita
Foundation (Stichting Krita). Trichromat is an independent product and is not
affiliated with Adobe or the Krita Foundation.
