# deadlock-radio-helper

A single static page used by a locally patched copy of the Deadlock Radio HUD mod to show the current song's duration.

Deadlock's in-game browser can no longer run scripts inside YouTube pages, and YouTube's embed player refuses pages without a real origin (error 153). This page provides that origin: it cues the video in a hidden embed (it never plays it), reads the duration, and reports it through the page title as `DLR:<videoId>:<seconds>`.

Usage: `https://samelliottdlt.github.io/deadlock-radio-helper/?v=<videoId>`

The repo also has `player.html`, which plays the video in the embed player so the mod can control volume and playback. It takes commands through its URL hash (`#<seq>:vol:<0-100>`, `fade`, `play`, `pause`, `next`, `prev`, `seek`) and reports state through its title as `DLP:<json>`.

Usage: `https://samelliottdlt.github.io/deadlock-radio-helper/player.html?v=<videoId>[&list=<playlistId>][&vol=<0-100>]`
