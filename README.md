# deadlock-radio-helper

Static pages used by a locally patched copy of the Deadlock Radio HUD mod.

Deadlock's in-game browser can no longer run scripts inside YouTube pages, and YouTube's embed player refuses pages without a real origin (error 153), so these pages provide that origin.

## app.html (current)

What the mod's Browser tab shows: a link box (paste a YouTube video, playlist, youtu.be or Shorts link, or a video ID), YouTube's embed player, and a list of recent links. The mod controls it by changing only the URL hash (`#<seq>:vol:<0-100>`, `fade:<0-100>:<seconds>`, `play`, `pause`, `next`, `prev`, `seek:<seconds>`) and reads its state from the page title (`DLP:<json>`).

## index.html, player.html (older experiments)

`index.html?v=<id>` reports a video's duration through its title as `DLR:<id>:<seconds>`. `player.html?v=<id>` is an earlier hidden-player version of `app.html`.
