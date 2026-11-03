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
