# Chiki Games: rules for every change to this repo

Sean's phone games, served by GitHub Pages at https://shawnchiki.github.io/games/. The headset apps live in the separate `xr` repo.

## Every push

1. **Commit message first line = what's new, in plain words.** It shows word for word on the launcher card.
   Format: `<Game name> vX.Y: <what changed, the part he'll notice first>`. One game per commit where possible.
2. **New game → its own folder (`name/index.html`) and a card in `index.html`:**
   `<a class="card" href="name/"><b>Game Name</b><span class="blurb">One line on what you do in it</span></a>`
3. **Every game page loads `../updated.js`** just before `</body>` (it shows when the game last changed, Toronto time).
4. Built for phones first: thumb controls, no hover-only actions, readable at 390px wide, uncluttered (no extra stats).
