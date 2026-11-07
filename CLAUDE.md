# Chiki Games: rules for every change to this repo

Sean's phone games, served by GitHub Pages at https://shawnchiki.github.io/games/. The headset apps live in the separate `xr` repo.

## Every push

1. **Commit message first line = what's new, in plain words.** It shows word for word on the launcher card.
   Format: `<Game name> vX.Y: <what changed, the part he'll notice first>`. One game per commit where possible.
2. **New game → its own folder (`name/index.html`) and a card in `index.html`, in the section that fits:**
   - **Multiplayer · Multiplatform** (`section.mp`): phones and the Quest really play together in one game
     (same PeerJS code prefix, or a Quest host that phones join). One `<div class="card" data-src="games:folder xr:file.html">`
     with a `.plat.ph` Phone button and a `.plat.qu` Quest button. `data-src` lists every path in either repo so "Updated" shows the newest side.
     Also give its card in the `xr` launcher a `<span class="xplay">Phone + Quest</span>` tag.
   - **Phone Games** (`section.phone`): everything else, solo or phone to phone:
     `<a class="card" href="name/"><b>Game Name</b><span class="blurb">One line on what you do in it</span></a>`
   - **Design tools are not games**: form-finding / modeling tools go on the **Design Tools** page, `tools/index.html`
     (https://shawnchiki.github.io/games/tools/). Sections: "On a screen" (phone/computer browser) and "In the headset"
     (links to the xr Modeling Tools). A tool hosted in this repo gets `data-src="games:tools/name"`, an xr one `data-src="xr:folder"`;
     a tool that only exists as a Claude artifact links to its artifact URL with no `data-src` (no "Updated" line).
3. **Every game page loads `../updated.js`** just before `</body>` (it shows when the game last changed, Toronto time).
4. Built for phones first: thumb controls, no hover-only actions, readable at 390px wide, uncluttered (no extra stats).

## Launcher look

"Arcade night", deliberately different from the Chiki XR Memphis look: deep indigo with a dot grid, rounded white keycap cards
with a colored edge underneath that press down (lime = Multiplayer · Multiplatform, sky blue = Phone Games), Lilita One + Nunito.
Design Tools has a third look, "drafting table": graph paper, thin ink lines, square cards with orange corner ticks, Space Grotesk + IBM Plex Mono.
The bar at the top links all three (Chiki Games, Chiki XR, Design Tools); keep it on every launcher, each in its own site's style.
