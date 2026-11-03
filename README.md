# Strechy

An interactive 3D character designer portfolio. Enter a name, pick one of three cartoon characters, then grab the face and stretch it like taffy. Push too hard and its patience runs out.

## Run it

It's a single static file. Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

It also works on GitHub Pages (Settings → Pages → deploy from `main`, root folder).

## How it works

- **Three.js (r128)** renders procedurally modelled characters with physical skin, hair, eye and lip materials.
- **Face stretching** is real mesh deformation in a custom vertex shader: up to 4 grab points with Gaussian falloff, volume-preserving thinning, recomputed normals, and spring physics for the wobble on release.
- **Mood system**: patience drains based on which region you pull, how far, how fast, and how often. At 0% the character goes furious, then recovers when left alone.
- **GSAP** handles the intro and UI transitions. Sound effects are synthesised with the Web Audio API.

Libraries load from cdnjs; fonts from Google Fonts.
