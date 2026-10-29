# deadlock-radio-helper

A single static page used by a locally patched copy of the Deadlock Radio HUD mod to show the current song's duration.

Deadlock's in-game browser can no longer run scripts inside YouTube pages, and YouTube's embed player refuses pages without a real origin (error 153). This page provides that origin: it cues the video in a hidden embed (it never plays it), reads the duration, and reports it through the page title as `DLR:<videoId>:<seconds>`.

Usage: `https://samelliottdlt.github.io/deadlock-radio-helper/?v=<videoId>`
