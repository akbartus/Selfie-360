<h1 align="center">Selfie 360</h1>

<p align="center"><b>A web based selife application allowing to make selfies on 360 photo backgrounds.</b></p>

## Features

:camera: **Upload  own 360 photo or use available one on Internet**: Upload own desired 360 photo (of any size) or decide to use the link to a 360 photo that is available on Internet.

:heavy_plus_sign: **Change perspective and zoom in or out**: Change the background/perspective and if necessary, zoom in or out.

## Usage
1. Copy the repository to your own server (local/online). 
2. Run it.
3. Upload your own 360 photo or add a link to 360 photo that is available online
4. Choose perspective, and if necessary, zoom in or out. 
5. Activate selfie by clicking a button
6. Decide whether to save or take a new photo

### Example

Build VR scenes in the browser with just a few lines of HTML! To start playing
and publishing now, remix the starter example on:

[![Remix](https://cloud.githubusercontent.com/assets/674727/24572421/688f7fc0-162d-11e7-8a35-b02bc050c043.jpg)](https://glitch.com/~aframe) [![Fork](https://user-images.githubusercontent.com/39342/52831020-d42dcb80-3087-11e9-833f-2d6191c69eb9.png)](https://repl.it/@dmarcos/aframe)

```html
<html>
  <head>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
      <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
      <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
      <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
      <a-sky color="#ECECEC"></a-sky>
    </a-scene>
  </body>
</html>
```

With A-Frame's [entity-component
architecture](https://aframe.io/docs/1.2.0/introduction/entity-component-system.html), we can drop in community
components from the ecosystem (e.g., ocean, physics) and plug them into our
objects straight from HTML:

[![Remix](https://cloud.githubusercontent.com/assets/674727/24572421/688f7fc0-162d-11e7-8a35-b02bc050c043.jpg)](https://glitch.com/~aframe-registry) [![Fork](https://user-images.githubusercontent.com/39342/52831020-d42dcb80-3087-11e9-833f-2d6191c69eb9.png)](https://repl.it/@dmarcos/aframe)

```html
<html>
  <head>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-particle-system-component@1.0.x/dist/aframe-particle-system-component.min.js"></script>
    <script src="https://unpkg.com/aframe-extras.ocean@%5E3.5.x/dist/aframe-extras.ocean.min.js"></script>
    <script src="https://unpkg.com/aframe-gradient-sky@1.2.0/dist/gradientsky.min.js"></script>
  </head>
  <body>
    <a-scene>
      <a-entity id="rain" particle-system="preset: rain; color: #24CAFF; particleCount: 5000"></a-entity>

      <a-entity id="sphere" geometry="primitive: sphere"
                material="color: #EFEFEF; shader: flat"
                position="0 0.15 -5"
                light="type: point; intensity: 5"
                animation="property: position; easing: easeInOutQuad; dir: alternate; dur: 1000; to: 0 -0.10 -5; loop: true"></a-entity>

      <a-entity id="ocean" ocean="density: 20; width: 50; depth: 50; speed: 4"
                material="color: #9CE3F9; opacity: 0.75; metalness: 0; roughness: 1"
                rotation="-90 0 0"></a-entity>

      <a-entity id="sky" geometry="primitive: sphere; radius: 5000"
                material="shader: gradient; topColor: 235 235 245; bottomColor: 185 185 210"
                scale="-1 1 1"></a-entity>

      <a-entity id="light" light="type: ambient; color: #888"></a-entity>
    </a-scene>
  </body>
</html>
```

### Builds

To use the latest stable build of A-Frame, include [`aframe.min.js`](https://aframe.io/releases/1.2.0/aframe.min.js):

```js
<head>
  <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
</head>
```

To check out the stable and master builds, see the [`dist/` folder](dist/).

### npm

```sh
npm install --save aframe
# Or yarn add aframe
```

```js
require('aframe')  // e.g., with Browserify or Webpack.
```

## Local Development

```sh
git clone https://github.com/aframevr/aframe.git  # Clone the repository.
cd aframe && npm install  # Install dependencies.
npm start  # Start the local development server.
```

And open in your browser **[http://localhost:9000](http://localhost:9000)**.

### Generating Builds

```sh
npm run dist
```

## Questions

For questions and support, [ask on StackOverflow](https://stackoverflow.com/questions/ask/?tags=aframe).

## Stay in Touch

- To hang out with the community, [join the A-Frame Slack](https://aframe.io/slack-invite/).
- [Follow `A Week of A-Frame` on the A-Frame blog](https://aframe.io/blog).
- [Follow @aframevr on Twitter](https://twitter.com/aframevr).
- [Subscribe to the Newsletter](https://aframe.io/subscribe/).

And get in touch with the maintainers!

- [Diego Marcos](https://twitter.com/dmarcos)
- [Don McCurdy](https://twitter.com/donrmccurdy)
- [Kevin Ngo](https://twitter.com/andgokevin)

## Contributing

Get involved! Check out the [Contributing Guide](CONTRIBUTING.md) for how to get started.

You can also support development by [buying a gorgeous A-Frame t-shirt with exclusive designs](https://teespring.com/stores/aframe)

## License

This program is free software and is distributed under an [MIT License](LICENSE).
