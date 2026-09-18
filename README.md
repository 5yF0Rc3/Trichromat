# Trichromat
Photoshop or Krita don't blend two colors, they average the RGB values, which wrong for real paint. Halfway between blue and yellow, RGB gives a dull grey. A palette gives green.

The second problem is the shape. Three colors mix over a triangle, and a triangle has a unbalanced middle: its center is twice as far from the corners as from the edges, so the two-color blends along the edges crowd the center while the corners sit far out. Trichromat mixes over a Reuleaux triangle instead. The edges bow outward as arcs. From the same three corners that gives 63 % more mixing area, and the edge blends move out to nearly the same distance from the center as the corners. The field reads evenly, and there is room to pick.

<p align="center">
  <img width="600" alt="Features" src="/images/Features with standart.png" />
</p>

**Trichromat** is a color mixer for Photoshop and Krita. Three colors sit in the corners of a field, every mixture of them lies in between. Click a mixture and it is your foreground color. The app floats above Photoshop or Krita, always on top. Can be switched off. Also works without a painting app: in Solo mode a pick copies the color as HEX.

### Mix models
**Spectral** (Kubelka–Munk, via spectral.js) is the default. Each color is treated as a pigment with a reflectance spectrum, and the mixture is computed from how those pigments absorb and scatter light together. Blue and yellow make green, complementary colors mute each other into browns and greys, and the tint-strength pad lets you decide which pigment dominates.

**OKL** blends linearly in OKLab, a perceptually uniform color space. Smooth, even steps, no dead grey zone in the middle and the hues stay clean.

**RGB** is the plain sRGB average, the math Photoshop and Krita use when they blend colors by default. It is the reference. Put the same three colors in and you see the muddy middle you have been working around.

### Lightness
One slider lightens or darkens the whole field. **Relative** shifts the value in OKHSL; hue and saturation stay. **White** mixes white in as a fourth pigment (Spectral only).

## Download and Requirement
**OS:** <ins>Windows 10/11</ins> or <ins>macOS 12</ins> or newer.

**For Photoshop:** <ins>Photoshop 26.2.0</ins> or newer versions required with the <ins>Creative Cloud</ins> desktop app. 

**For Krita:** <ins>Krita 5.2</ins> or newer. Tested on 5.3 and 6.0.

**Download:** [Get it on Gumroad](https://745191790950.gumroad.com/l/trichromat)


## Install
### 1. The app
Extract the zip to a folder.

#### Windows
Windows SmartScreen shows "Windows protected your PC". Click `More info`, then `Run anyway`. The installer asks for the install folder and creates a Start menu and desktop shortcut.

#### MacOS
Open the `.dmg` that matches your Mac (`arm64` for Apple Silicon, `x64` for Intel) and drag Trichromat to *Applications*. 

> [!IMPORTANT]
> The app is not yet notarized, so the first launch is blocked. Open `System Settings → Privacy & Security`, scroll down to the message about Trichromat and click `Open Anyway`, then confirm. This is needed once.
> 
> <img width="300" alt="apple 2" src="/images/apple 2.png" />


### 2. The plugin
The App has to be started once, to be visible for the plugin.

#### Photoshop
Double-click `Trichromat-Bridge.ccx`. The Creative Cloud desktop app installs it and warns that the plugin was not verified by Adobe; **confirm**.
In Photoshop open `Plugins → Trichromat Bridge`.

If the app is not running, the panel's *Open Trichromat* button starts it.
Photoshop asks for permission the first time.

#### Krita
In Krita choose `Tools → Scripts → Import Python Plugin from File…` and pick
`Trichromat-Krita-<version>.zip` from the download. Restart Krita.

`Settings → Dockers → Trichromat Bridge` opens a small docker with the
connection status and an *Open Trichromat* button. The connection works
without the docker open.

<img width="300" alt="krita anstallation" src="/images/krita install 1.png" />

If its not visible go to`Settings → Configure Krita → Python Plugin Manager`, tick **Trichromat
Bridge**.

### 3. Activate

On the first start the app asks for your license key. It is in the **Gumroad**
receipt e-mail and in your Gumroad library. Copy the key, click *Paste* in
the app, then *Activate*. Activation needs an internet connection once; afterwards the app
re-checks the key in the background from time to time.

### Updates
The app checks for a new version on start and shows it on the settings page.
Download the new build from your [Gumroad library](https://gumroad.com/library) and run the installer over
the old one. 

## Guide

<p align="center">
  <img width="600" alt="krita anstallation" src="/images/Tutorial.png" />
</p>


### Color Field

Click anywhere in the field to pick a color. While Trichromat is linked to
Photoshop or Krita, the picked color becomes the foreground color; hold **Alt**
while clicking to set the background color instead. You can also drag: the
color is sent when you release.

### Color Corner

The three corner are your palette. Each corner has two halves. Click the **bottom
half** (the swatch) to load the current foreground color from Photoshop or
Krita into that. Click the **top half** (the letter) to select it.

#### Sliders
The sliders edit the selected corner for hue, saturation and lightness directly.

#### Flash Icon
The bottom corner carries a **flash** icon. Switch it on and every color you pick in your painting app is written into this automatically.

### Readout & Solo mode

The readout shows the picked color with its HEX and RGB values. Click the HEX
value to copy it to the clipboard.

Trichromat also works without a painting app. In **Solo mode** a click in the field copies the hex directly, and the readout swatch becomes selectable: click
it to fine-tune the picked color with the sliders. While you do that, the selector ring in the field disappears, because the tweaked color is no longer a point in the field. Click in the field to bring it back.

### Model

- **Spectral** mixes the corners as pigments, based on Kubelka–Munk theory,
  the way physical paint behaves: blue and yellow give green.
- **OKL** blends linearly in OKLab, a perceptually uniform color space: smooth,
  even steps, clean hues. How light mixes, done right.
- **RGB** is the plain sRGB average, the same limited blend most other software
  does.

### Lightness

The slider lightens or darkens the entire field at once. **Relative** shifts
the lightness of the mixed colors while hue and saturation stay, and it works
in both directions. **White**, available in Spectral, adds white as a pigment
to the mix.

### Tint strength

Not every pigment is equally strong. Turn on the tint control and drag the dot
to change the relative strength of the three pigments. The center is
neutral. Alt-click the button to reset.

### Background

Switch the button and the sliders edit the color around the field instead
of a corner.

### Connection

The connection page switches between **LINKED** (talking to Photoshop or Krita)
and **SOLO** (standalone). The status dot tells you where you are:

- **Green**: linked to a painting app.
- **Orange**: connecting, give it a moment.
- **Red**: no connection found. Open the Trichromat Bridge panel in your
  painting app and check it is running, **RESTART** if needed.
- **Blue**: Solo mode. Trichromat is not searching for an app; picks go to
  the clipboard and the flash and load-from-app functions are off.

## Reporting problems or ideas

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
