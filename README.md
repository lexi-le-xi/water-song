# Water Song

An interactive lake surface played with your hands. Tap your fingers in front of the webcam like playing piano: each tap sends ripples across a sunlit green pond and sounds a water "glug" tuned to D minor, over a babbling spring, passing wind and birdsong.

**Live:** https://lexi-le-xi.github.io/water-song/

## Playing

- Click **Click to begin** and allow the camera.
- The ten fingers are ten notes, left pinky to right pinky: D4 E F G A | B♭ C D5 E F5.
- Faster taps are louder and sharper; deeper presses make bigger ripples.
- No camera? Click the water, or press **1–0** to play the ten notes.
- Keys: **C** camera preview · **M** mute · **F** fullscreen.

Works best in Chrome. The camera only works over `https://` or `localhost`.

## How it works

- **Water:** WebGL2 height-field wave simulation for the ripples, over procedural wind-driven waves refracting a reflected leaf canopy.
- **Hands:** MediaPipe Hand Landmarker tracks all ten fingertips; a tap is a quick downward stroke of a fingertip relative to its knuckle.
- **Sound:** synthesized in real time with Web Audio. The spring and the taps are built from individual bubbles ringing at their Minnaert frequency (van den Doel, 2005); wind is filtered noise in gusts; birds are synthesized calls.

## Running locally

```bash
python3 -m http.server 8642
```

Then open http://localhost:8642.
