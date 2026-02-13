# updater

Updater is an app for fetching and installing system updates on bootc systems and managing automatic updates. Updater is designed as a replacement for GNOME Software and Discover's built in update management. Updater is being designed for Apollo, but will avoid relying on specific functionality. It will be configurable for other bootc-based images to use too.

## Planned features
- Check, fetch and apply bootc, fwupd and Flatpak updates
- Toggle automatic updates on the system
- Allow the user to enable/disable "features", and choose between set images (e.g., dev mode, Nvidia drivers) chosen by the image vendor.
- Choose between image update channels, such as stable, testing, etc.
- Rolling back images in the case of an issue

## Out of scope/not currently planned
- Management of brew packages, users using the CLI should be fine running `brew update`
- Management of updates on package-based systems
- A/B systems other than bootc (at first, this may be reconsidered long-term)
