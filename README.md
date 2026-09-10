# Paranoid Android

A small, sad robot called *7yuc zhd* who reacts to your cursor all wrong. It recoils when you come
near, drifts back toward you when you leave, and trembles the longer you hold still.
It remembers how you treated it between visits, and how long you were gone.

A tiny study in anxiety, loosely haunted by a Radiohead song. No lyrics are
reproduced; only the mood.

## Run it

Open `paranoid-android.html` in any modern browser. That's the whole thing: one
self-contained file, no build step, no dependencies, no server.

To put it online, drop the file on any static host (GitHub Pages, Netlify,
Cloudflare Pages) and share the URL.

## How it behaves

- **Come close** and it flinches away, harder the nearer you get.
- **Leave it alone** and it reluctantly drifts back toward where your cursor last was.
- **Hold still** and its unease climbs; the silence unsettles it more than movement.
- **Its thoughts** surface above its head, drawn from its current state.

## It remembers you

A `trust` value (shown bottom-left, ranging -1 to +1) persists in your browser via
`localStorage`. Crowding or cornering it drives trust down; a calm, respectful
presence builds it up. That value shapes how it greets and behaves toward you next
time. It also knows how long you were away, and absence slowly erodes the
relationship back toward a wary stranger.

Because the memory is stored per browser, each visitor gets their own private robot
that remembers only them. Private windows and some browsers that block third-party
storage (notably Safari inside an iframe) may not retain it.

## Notes

- Fully client-side. Nothing is sent anywhere; the memory never leaves your browser.
- Respects `prefers-reduced-motion`.
- Cursor-driven, so it currently does nothing on touch-only devices.
