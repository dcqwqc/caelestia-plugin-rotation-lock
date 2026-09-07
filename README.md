# RotationLock

Rotation lock for a convertible, as a Caelestia quick toggle.

The `yoga-tablet` daemon owns the lock, and other things flip it — a keybind,
folding the hinge — so this never caches a guess. It re-reads the daemon's state
whenever the toggle comes back on screen, and again after every write.

Where the daemon is not installed or not answering, the toggle hides itself
rather than sitting there dead. Nothing to configure.

## Requires

The `yoga-tablet` daemon from [kagami](https://github.com/dcqwqc/kagami).

## Status

Caelestia's plugin loader is not released yet — it lives on upstream's unmerged
`feat/plugins` branch, and the Plugins page there is still a mockup rendering
four fake cards. Nothing here can load until that lands.

It is built against the real schema rather than a guess at it: manifest keys and
the entry point type strings are taken from that branch's parser, so this should
need renaming rather than rewriting when the API ships.

## Install

Clone into Caelestia's plugin directory:

    git clone https://github.com/dcqwqc/caelestia-plugin-rotation-lock ~/.local/share/caelestia/plugins/rotation-lock

Or clone anywhere and add the parent to `path` in
`~/.config/caelestia/plugins.json`.

## Licence

GPL-3.0-or-later, matching Caelestia.
