# Changelog

All notable changes to Trichromat. One version number covers the app and
both Bridge plugins; a release says which plugin has to be reinstalled.

## Unreleased

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
