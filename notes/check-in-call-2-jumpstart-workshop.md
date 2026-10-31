# Haven Jumpstart Workshop — Godot 2D platformer (after Check-in Call #2) — detailed notes

| | |
|---|---|
| **Recorded** | Sat 19 Sep 2026 15:48 UTC = **Sun 20 Sep 2026, 1:48 AM AEST** (Canberra; before daylight saving began) = Sat 19 Sep 11:48 AM EDT. Straight after [check-in call #2](check-in-call-2.md) |
| **Length** | ≈ 43.7 min (≈ 38 min workshop + ≈ 5 min Q&A) |
| **Transcript** | [`transcripts/check-in-call-2-part2.md`](../transcripts/check-in-call-2-part2.md) (machine-generated; may contain errors) |
| **Presenter** | **Estella** (name tag "Estella Gu"; the hosts thank "Estella" for the workshop). A Haven staff member hosted/answered questions. Lines aren't attributed in the transcript. |
| **What it is** | A screen-share walkthrough of building the **Jumpstart "Godot platformer"**: a little character that runs and jumps around a tile-based level. Organizers need to finish **Jumpstart** (the game-making tutorial that is part of Haven prep; see the call 2 notes for the deadline) before they run a Haven. |

**How to read:** `[mm:ss]` = time from start of the recording. Everything is audio plus what's visible on the shared screen (Godot 4.x on a Mac — shortcuts are Command-based). `[unclear]` = couldn't be made out.

## TL;DR

- Build a **2D platformer in Godot** in ~25 minutes: `Main` node → `Player` (CharacterBody2D + Sprite2D + CollisionShape2D) → `TileMapLayer` with a TileSet and a physics layer → a script from the *CharacterBody2D: Basic Movement* template → tweak speed/jump/gravity → add a `Camera2D`.
- After that the presenter suggests **making it your own**: your own theme and assets, collectibles, enemies, scoring, sound effects; YouTube/Google tutorials for everything else.
- **Submit your Jumpstart through the file submission on the Jumpstart website** (the presenter also says organizers must submit Jumpstart *before* they organize).
- The tutorial page is at `jams.hackclub.com/jam/godot-platformer`; the Jumpstart site is `haven.jumpstart.hackclub.com`; ask questions in the **Jumpstart-Haven** Slack channel.
- Q&A: the team-size rule is a trial policy that "could change" and will be confirmed on a later call (see below); **every participant must ship a game on itch.io**, though hardware (macropad, handheld console) is welcome too.

## Action-item checklist

- [ ] Download **Godot** and follow the tutorial: `jams.hackclub.com/jam/godot-platformer` (step list; "step five" covers the physics layer)
- [ ] Finish and **submit Jumpstart** via the file submission on `haven.jumpstart.hackclub.com`
- [ ] Join the **Jumpstart-Haven** Slack channel to share your build and get help
- [ ] Extend your game: collectibles, enemies, scoring, sound effects, your own art

## Walkthrough, in order

### [00:00–03:00] Setup and tour of the editor
- The Godot **start screen** (after downloading Godot) → **Create New Project**. Name it anything; the example is a "space platformer". Choose a **project path** (the presenter keeps all their games in one folder; create a folder if you like).
- Renderer: **Forward+** — "a good in-between" — then **Create**.
- If you have questions or want a pause, **send a chat message**.
- **Main interface** (looks overwhelming at first): the **Scene** area (Godot uses **nodes** — "basically things" with lots of properties); the **File System** panel at the bottom-left (your files: nodes, tileset images, your own assets/animations/sounds); the **mode tabs** at the top — pick **2D** (this is a 2D platformer). The light purple rectangle is the **game view**.

### [03:00–05:40] The Main node and Player
- Create a root node: **Other Node** → the first option (a plain node; spoken as "the white circle") and **rename it `main`**. **Save** the project (Cmd-S / File → Save).
- Add the player under it with **plus**: **CharacterBody2D** — "the one used most for having a player in the game". Rename it `player`.
- Under `player`, add a **Sprite2D** (displays an image). For now use the **default Godot icon** from the File System: drag it into the **Texture** property in the Inspector; it appears in the game view. Later you can import your own images and drag them in.
- Shortcuts: the **plus** button in the Scene panel, or **Cmd-A**, to add a node. Late joiners can catch up with the link the presenter posted in chat.

### [05:40–09:30] Collision shape and first run
- The `player` shows an **error: the node has no shape** and can't collide. Fix it by adding a **CollisionShape2D** under `player` (so the engine knows the player's bounds and it doesn't fall through the floor); a polygon shape is available for more complex characters.
- In the Inspector set **Shape → Rectangle** and drag the **red dots** to cover the player.
- **Run** the game: the **Play** button top-right (or **Cmd-B**); it asks which scene — choose **Select Current**. Your player appears. (A viewer reminder: editor navigation is two-finger pan/zoom; Cmd-B plays.)

### [09:30–19:20] Build the level: TileMapLayer, TileSet, physics
- Under `main` add a **TileMapLayer** ("think of Minecraft: pick blocks and build levels instead of building by hand").
- With it selected, in the Inspector click the arrow next to **Tile Set → New TileSet**. A tileset is a set of blocks; the presenter shows the one they made earlier for a space platformer.
- For the demo, take a **screenshot of a plain green area** as `grass`, **drag the image into the File System**, then **drag it into the TileSet panel** at the bottom; when asked about automatically creating tiles, answer **Yes**. (Later, keep images/sounds in folders.) There was **video lag around 11:40–14:30**, and the presenter **paused the recording** and redid the tileset step.
- **Collision for the tiles:** in the Inspector open **Tile Set → Physics Layers → Add Element** to create a physics (collision) layer; then in the TileSet panel's **Paint** tab choose **Physics Layer 0** under *Paint Properties* and **paint over all your blocks** (later you can alter the collision shape for rounded corners, e.g. a winter theme). If you don't see a physics layer, make sure it's been added in the TileSet's Physics Layers (tutorial step five).
- **Design the level:** switch to the **TileMap** tab at the bottom, pick a block, and use the **pencil/paint tools** (and fill tools) to draw platforms — floating platforms etc. To make blocks bigger use **Transform → Scale** in the Inspector.
- Run again: the player just floats — it needs code.

### [19:20–29:30] The player script (Character Body 2D "Basic Movement" template)
- Select `player`, click the **scroll icon with the green plus** (Attach Script). Name it **`player.gd`**, tick **Template**, and choose **CharacterBody2D: Basic Movement**; **Create**. Godot switches to the **Script** workspace (use the top tabs to switch back to **2D**).
- Run: the player now **falls and moves with left/right and space**, but the feel is meh.
- **Code walkthrough:**
  - `extends CharacterBody2D` ties the script to the player node.
  - **`SPEED`** and **`JUMP_VELOCITY`** are **constants** (don't change during the game; things like a coin counter would be variables). Speed = how fast; jump velocity = how high — it's **negative** because in the coordinate system going up is more negative (e.g. change it to **−800** to jump about twice as high).
  - The big function is the **physics**: if the player is **not on the floor**, velocity falls according to **gravity**; if **jump (space) is pressed and on the floor**, add the jump velocity to the vertical velocity.
  - **Left/right:** a `direction` variable (−1 left, +1 right); if there's a direction, set horizontal velocity to direction × speed; otherwise **move velocity toward zero** so the player comes to a stop.
  - **`move_and_slide()`** (asked about in Q&A at ~[28:50]) "runs the whole process at the end" — it applies the movement.

### [29:30–33:10] Polish: speed/jump, gravity, camera
- The presenter edited **speed and jump velocity**; jumping felt "airy". To change **gravity**: **Project → Project Settings →** search "gravity" **→ Physics 2D → Default Gravity** — set it to about **2,500** for a snappier feel; "tweak around and see what you like".
- **Camera:** add a **Camera2D** under `player` (plus button). Back in 2D view, the pink rectangle is the camera view — it follows the player so you can build long levels. For a **camera lag effect**, select the Camera2D → Inspector → turn on **Position Smoothing** and set a small value.

### [33:10–34:40] Done — ideas and submission
- This ends the **base of the platformer**; now "go crazy": pick a **theme**, draw or find your own assets, add **collectibles**, **enemies**, **scoring**, **sound effects**; there are "tons of tutorials online".
- **Submission:** once finished, use the **file submission on the website**. The hosts thank the presenter and attendees. (At ≈[30:42] a host adds that organizers submit Jumpstart before they organize.)

### [34:40–38:30] Q&A about further resources
- **Q:** The Jumpstart website says the original Jumpstart event had more in-depth Godot tutorials, but they're not there now; where can we find more focused resources beyond what's available, especially if we've already advanced our game? **A:** The presenter says they built their first game last year (at a Hack Club hackathon in China) mostly from **YouTube tutorials** — search and you'll find a lot; they don't remember the specific channel but will **share resources in the Jumpstart-Haven Slack channel**.
- Hosts: join **Jumpstart-Haven** to share your builds. "Bye everybody"; a host stays on for further questions about Haven or Jumpstart.

### [38:30–43:35] Q&A about team size and what to ship
- One attendee (audio was patchy) asked about **team size**: someone on a team was saying two participants, but they thought three. A host asked them to type it in chat, then answered: **"right now we're trying a policy"** on team size that "could be subject to change", to be **confirmed in a future check-in call as we get closer to the event** (the figure itself isn't intelligible in the audio [unclear]; call 3 mentions up to three).
- Clarification: **Haven is a game-jam hackathon** — if someone wants to make hardware (e.g. a **macropad to play the game**, or their own game console) that's fine, but **all participants should ship a game, because it needs to be on itch.io**; "as long as it's a game, it's all good".
- The host ends the Zoom: "see you all next week".

## Links and resources
- `jams.hackclub.com/jam/godot-platformer` — Godot platformer tutorial steps (posted in chat; also the page the presenter mentions repeatedly for catching up)
- `haven.jumpstart.hackclub.com` — Jumpstart site with the file submission
- `hack.club/haven-c2` — call 2 check-in form (also in chat)
- Slack: Jumpstart-Haven channel (presenter will post resources there)

## Gaps / uncertainty
Several stretches (esp. ≈[11:40–14:30], ≈[39:00–42:00]) were affected by lag/poor audio and some Q&A phrasing is partial. The exact team-size number wasn't clearly audible. Screen details come from the audio plus video frames and may miss small on-screen text.
