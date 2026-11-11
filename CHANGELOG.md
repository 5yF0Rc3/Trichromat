# Changelog

All notable changes to Trichromat. One version number covers the app and
every Bridge plugin; a release says which plugin has to be reinstalled.

## Unreleased

## 0.3.0 — Blender and the palette, 2026-11-11

**Reinstall every plugin from this download.** The Photoshop Bridge `.ccx`
and the Krita plugin are new, and the Blender plugin ships for the first
time. From this version on, a plugin's panel warns when its version and the
app's differ and says which of the two to update.

### New

- **Blender support.** A Trichromat Bridge extension for Blender 5.0 and
  newer, in Texture Paint mode. Drag `Trichromat-Blender-0.3.0.zip` into the
  viewport, or use *Edit → Preferences → Add-ons*, the arrow menu at the top
  right, *Install from Disk…*. In Texture Paint press `N` and open the
  *Trichromat* tab.
- **Palette**, a second mix screen next to the field. Place discs and
  rectangles of color; where they overlap, they mix, in all three models.
  **+** adds a shape in your foreground color, **Fill** loads the foreground
  into the selected one. Each shape has its own **TINT** (turned down, it
  becomes a glaze) and **SMOOTH** (a smooth fade, or 2 to 16 bands).
- **Background mix.** The row next to the readout mixes the background color
  into the field as a fourth color, in every model. A white background mixes
  white in like white paint, a dark one darkens, any other color tints. The
  row collapses to give the field more room.
- **Readout chip.** Select the readout's swatch and SAT and LIGHT shift all
  three corners, or every shape on the palette, together, relative to where
  they are.
- **SEND COLORS TO ALL CONNECTED APPS** on the settings page. With two or
  three painting apps connected, every color you send reaches all of them,
  not only the active one.
- The plugin panels show their **version number**.

### Changed

- The **LIGHTNESS** slider and its Relative and White modes are gone. The
  background mix with a white background replaces White; the readout's SAT
  and LIGHT shift replaces Relative.
- The corner chips and the field sit closer to the window edge, so the field
  is larger. The window can be made a little lower (380 instead of 400).
- Text buttons carry an outline at rest, like the segmented controls;
  selection, switches and the screen-switch icons are redrawn.
- The Krita and Blender plugins are free software under the GNU GPL,
  version 3 or later; the license text ships in each plugin as
  `LICENSE.txt`. The EULA and the privacy notes now cover Krita and Blender.

### Fixed

- Releasing HUE, SAT or LIGHT now sends the color under the selector to your
  painting app. Before, only the readout followed and the foreground kept
  the old pick.
- With the **flash** on, a new foreground from your painting app also moves
  the selector onto corner C, so the readout shows exactly that color
  instead of a mix of it.

## 0.2.0 — Krita, 2026-09-18

**Reinstall both plugins from this download.** The Photoshop Bridge `.ccx`
is new, and the Krita plugin ships for the first time. An older Photoshop
panel still connects, but it no longer retries on its own after the app
was closed.

### New

- **Krita support.** A Trichromat Bridge plugin for Krita 5.2 and newer.
  Import `Trichromat-Krita-0.2.0.zip` in Krita (*Tools → Scripts → Import
  Python Plugin from File…*), restart, then enable it in the Python Plugin
  Manager if it is not on already. `Settings → Dockers → Trichromat Bridge`
  shows the connection and opens the app.
- **Window pin** in the title bar. Pinned, the app floats over your canvas
  and never takes the keyboard. Unpinned, it is an ordinary window that can
  take focus. Remembered between starts.
- **SCALE** on the settings page (100 / 125 / 150 / 200 %): a bigger window
  and UI for 4K displays and screen recordings.
- **Solo mode: copy HEX to clipboard on click** can be switched off on the
  settings page. Clicking the HEX value still copies it.
- **Settings are remembered** between starts: markings, resolution, scale,
  the window pin and the solo-mode copy switch.

### Changed

- The connection page's toggle reads **LINKED** instead of PHOTOSHOP, and
  the line under it names the app you are connected to.
- The **UPDATE** notice moved from the settings page to the title bar, next
  to the version. It only shows while there is a release to download.
- Sharper mixing field on high-resolution displays.
- The mark at the centre of the field is a dot instead of a tick.
- The button next to the lightness slider is called **tint strength**, as
  in the guide, instead of *grey point*.
- Mix page labels read **LIGHTNESS** and **MODEL**.
- Buttons and the title bar redrawn per the design; INFOS & HELP on the
  settings page opens the project page.

### Fixed

- The Photoshop panel reconnects on its own again after the app was closed
  and reopened. It said *Retrying…* before, but did not.
- The activation screen takes the keyboard while it is up, so the license
  key can be typed or pasted into the field even with the window pinned.
- The lightness slider's value bubble stays on the slider after a resize.

## 0.1.0 — first beta, 2026-09-09 (app 0.1.0, bridge 0.1.0)

- Reuleaux mixing field with three corner colors and Kubelka–Munk mixing.
- OK-space lightness control, grey-point mode, corner pinning.
- Photoshop foreground and background set on release, solo mode copies hex.
- Settings page with markings toggle, resolution and version.
- License activation and update notice.
