# Stick Head — Planet Prototype

A tiny 3D platformer made for phones. You play a little guy with an analog stick on his head, running around a planet that turns out to be a giant version of his own head.

**Play it:** https://pablokm.github.io/Tuto/

## Controls

| Action | Phone | Keyboard |
| --- | --- | --- |
| Start | Tap anywhere | Any key |
| Run | Drag the head-shaped stick (bottom-left) | WASD / arrow keys |
| Jump / flip | ⬆ button (press again in the air to flip) | Space |
| Glide | Hold ⬆ while falling | Hold Space |
| Electric run | ⚡ button (tap to toggle) | Hold Shift |
| Pick up / throw | ✋ button (dinosaurs or other players) | F or Enter |
| Ride a dinosaur | Land on its back · jump to hop off | |
| Look around | Drag anywhere else | Q / E |
| Zoom | Pinch | Mouse wheel |

## Play together

Tap the two-people button (top right), then **Start a room** and send the 4-letter code or invite link to a friend. They tap **Join** (or just open the link) and you share the same planet: up to four players, each Tuto in their own colour. Phones connect directly to each other through PeerJS; if a pair can't connect on mobile data, try Wi-Fi.

## Modes: hold Tuto

Press and hold a finger on Tuto and four floppy discs float up in front of him. Walk up to one and press the ✋ button (or just tap it) and he gets zapped inside:

- 🔵 **Tuto AR**: the AR sandbox (`ar/`).
- 🔴 **Tuto Hoboken**: Stick Head in Hoboken (`nj/`).
- 🟠 **Tuto Motion**: motion capture. Start the camera and a stick-figure skeleton is drawn over you while the left Tuto copies you live. ⏺ records, and the right Tuto replays the clip. Save clips on your phone, or export a `.bvh` (Blender and game engines) or `tuto-motion.json` (MediaPipe landmarks plus the motion already solved into Tuto's bones, elbows and knees included) to animate a game character. Needs internet the first time (it downloads the pose finder). *Try demo* runs a built-in dancer with no camera.
- 🟡 **Tuto Maker**: a tiny Blender inside the platformer. In a white void (Tuto is 4 units tall) press ● to drop a point 3 units in front of him (▲▼ move the pink dot up and down), ╱ to link points with lines, and ▰ (or close the loop) to fill them into a solid plane. Tuto can stand on what you build. The stage grows as you build. ☰ has colours, **Explore** mode, save/load, and export as `.gltf`, `.obj` or `.json`.

The ⏏ button brings you back to the planet.

Tuto has two-segment arms and legs everywhere (planet, AR, Hoboken, Maker, Motion): elbows and knees bend as he runs, jumps, flips and rides.

## Things to try

- Bounce off the giant nose to land on top of the stick.
- Stand on the planet's eyes or mouth.
- Stand still for a while.
- Jump on a dinosaur's back.

## Also here: Stick Head — Garden State

Stick Head in Hoboken, New Jersey: run up buildings, bounce off trees, talk to the locals, or load any real OpenStreetMap file with the 🗺 button.

**Play it:** https://pablokm.github.io/Tuto/nj/

Hoboken's layout is hand-built from the real street grid (approximate). Imported maps: © OpenStreetMap contributors (ODbL). It lives in the `nj/` folder.

## Also here: Stick Head AR

Stick Head in your own room, through your phone's camera. Drop him on the floor, run him around with the same moves, put down boxes to wall-run up and bouncy trees, and pinch to resize him.

**Play it:** https://pablokm.github.io/Tuto/ar/

On Android Chrome he's tracked on your real floor (WebXR), so you can walk around him. On iPhone and other browsers it uses the camera plus your phone's tilt, so he stays put while you look around but doesn't follow you if you walk. It lives in the `ar/` folder.

Built with [three.js](https://threejs.org/). Everything is in `index.html`.

## Sid Dash

A 3D endless runner by the Trouble Makers. Swipe left/right to change lanes, swipe up to jump & flip, and collect all 3 stars to reach the next stage.

**Play it:** https://pablokm.github.io/Tuto/sid-dash/

### Tuto Maker: first person + touch select
- Tap a point to select it (cyan); Line / Delete then use it. While drawing a line, tapping a point links it.
- Hold **Look** to see through Tuto's eyes: the stick aims the camera, ▲▼ set distance, height follows where he looks. Quick-tap Look to latch it on.

### Tuto Maker: reshaping
- Hold a point or a line for a moment, then drag to move it (snaps to the grid, planes follow). Undo reverts it.
- The ⇄ button switches dragging between **Floor** (slide on the ground) and **Wall** (move up/down).
- Messages now pop up at the top of the screen, and the menu panel slides up from the bottom.

### Tuto Maker: grabbing, solid planes, moves
- **Grab** (✋, or F): Tuto locks on to the nearest point or line in reach (a cyan ring shows which) and grabs it. Something at his feet makes him crouch; something overhead makes him hang by his hands. The stick drags it (Floor/Wall button picks the direction). Tap Grab again to let go, or **Jump** to leap off it.
- **Solid** (▣): planes block Tuto from the sides and from below. Off = he can walk through them (he still lands on top).
- Float (hold Jump while falling) and the double-jump flip work in Maker now too.

### Tuto Maker: shooting points
- Tap **●** to drop a point ahead of Tuto. **Hold** it and Tuto winds up a jump shot (dotted arc shows the flight; hold longer = farther). Let go and he hops, extends, flicks, and the point flies in an arc in the direction he faces (or where you aim in Look mode).
- While it flies, any other input (stick, jump, any button or key) freezes it in the air as a real point. If nothing interrupts it, it freezes where it lands.

### Tuto Maker: layout and plane tools
- Height slider (left, above the stick) sets how high new points go. **●** is a round button left of Jump (tap = place, hold = shoot, with a fadeaway lean and a kicked-out leg). Menu is the ☰ at the top right; the triangle at the top left goes back to the planet. Counts show at the top of the screen.
- Hold a plane: R / S / T / E pop up. Slide onto one and let go to get its controls: **Rotate** (axis + angle), **Scale** (all or one axis), **Transform** (X/Y/Z move), **Extrude** (pulls the plane out along its normal and adds the side walls). ✓ applies (Undo reverts), ✕ cancels.
- Solid planes now also push Tuto back out if one ends up inside him, and block him at corners and from below.

### Tuto Maker: rival Tuto
- **Foe** (😠) spawns a purple rival (up to 3; a 4th tap sends them home). It chases Tuto and lunges to grab him: caught Tuto is held in front of it. Tap **Jump** 3 times to break free (it gets stunned), or wait and it throws him.
- If a plane is in its way, the rival punches and kicks it. Each hit tints the plane redder; the 3rd hit shatters it into pieces (Undo brings it back).

## Tuto Jam (purple floppy)
Grab the purple **JAM** disc to drop into a band room with four Tutos: singer (mic + guitar), pianist, drummer and bassist. Tap one to take over their instrument: piano keys, drum pads, a bass fretboard, or a singer with a voice strip (with vowels) plus guitar chords. The other three accompany you. Hit **Rec** to capture the mix, then **▶ Play take** or **⬇ MP3** to export it (needs the lamejs encoder from jsdelivr; the artifact viewer may block mp3 downloads, the GitHub Pages version works).

### Jam together
Tap **👥 Play together** in Jam to start or join a room (same codes as the planet). Everyone who is in Jam shares the band: you each pick an instrument (a **P1/P2…** tag shows who is on what), the backing band mutes any part a real player has taken, tempo is shared, and everyone's notes are heard live. Each player can record their own mix. Notes travel over the room's presence channel, so expect a little network lag.
