DOOM ENGINE WEB PORT - LOCAL FOLDER EDITION
============================================

Plays Doom, Doom II, Final Doom, Freedoom, Heretic, Hexen and Strife in your
browser. The game data isn't included: put your own .wad files in this folder.

1. Copy your WADs here, next to index.html (or into the "wads" folder), e.g.
     doom2.wad   heretic.wad   hexen.wad   strife1.wad   voices.wad
2. Start the local server:
     Mac:      double-click start-server.command
               (first time: right-click > Open, because it's a downloaded script)
     Windows:  double-click start-server.bat
     Anything: python3 serve.py        (optional port: python3 serve.py 8080)
   Your browser opens http://localhost:8000 with every game in the folder listed.
3. Click a game. Tick any add-ons first (e.g. hexdd.wad for Hexen: Deathkings,
   or Doom PWAD mods). Strife picks up voices.wad automatically.

Other web servers work too (nginx, Apache, Caddy, `npx serve`, VS Code Live
Server). With a server that shows folder listings, any .wad name is found.
Without listings, the page looks for the standard names (doom2.wad, tnt.wad,
heretic.wad, hexen.wad, strife1.wad, ...), or you can add a wads.json file
listing your files: ["doom2.wad", "wads/mymod.wad"].

Opening index.html straight from disk (file://) still works, but browsers
won't let the page look in its folder, so you'd pick the WAD by hand.

Saves and settings are stored in the browser, separately for each WAD.
Engines: doomgeneric and Chocolate Doom, GPLv2 (source in doom-web-src.zip).
