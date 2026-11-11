# Privacy

Last updated: 2026-11-10

Trichromat is a desktop application. It does not have user accounts and it
does not collect analytics.

## What leaves your computer

- **License verification.** When you activate the app and periodically
  afterwards, the app sends your license key to Gumroad's license
  verification service (`api.gumroad.com`) and receives the purchase status
  back (valid, refunded, and similar). Gumroad's own privacy policy applies to
  that service.
- **Update check.** On start and about once a day the app downloads a small
  version file from this GitHub repository to see whether a newer version
  exists. GitHub sees the usual request metadata such as your IP address.

## What stays on your computer

Colors, documents, palettes, settings and the license key itself are stored
locally only. The app and its plugins for Photoshop, Krita and Blender talk
over a connection on your own machine (`localhost`) and never over the
network. The plugins send nothing anywhere else. Blender lists the
extension as using the network: that permission covers only this local
connection.

## Contact

Questions about privacy: open an issue in this repository or use the support
address on the Gumroad product page.
