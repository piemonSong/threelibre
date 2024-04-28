# `Threelibre`

A **[*Three.js*](https://threejs.org/)** plugin for **[*MapLibre GL JS*](https://maplibre.org/maplibre-gl-js/docs/)** and **[*Azure Maps*](https://azure.microsoft.com/en-us/services/azure-maps/)** using the [`CustomLayerInterface`](https://maplibre.org/maplibre-gl-js/docs/API/interfaces/CustomLayerInterface/) feature. Provides convenient methods to manage objects in lnglat coordinates, and to synchronize the map and scene cameras.
<img alt="threebox" src="docs/gallery.jpg">

<br>

- - -
## Latest release

Threelibre is  available as an **npm package** 

```js
npm i threelibre-plugin
```
<br>

- - -

## Example

|Models built-in & custom animations |Mouse over/out, Selected, Drag&Drop, Drag&Rotate, Wireframe 
---------|-----------------------
|<img alt="threebox" src="https://i.postimg.cc/vTNLLLLn/Animation-Video.gif" width="100%">|<img alt="threebox" src="https://i.postimg.cc/3Jjgnvjz/Wireframes.gif" width="100%" >

|Tooltips using altitude|Optimization of camera perspective and depth
|----------|-------
|<img alt="threebox" src="https://i.postimg.cc/wM7DvR8j/Labels-On-Height.gif" width="100%">|<img alt="threebox" src="https://i.postimg.cc/zB9nPwcY/Depth.gif" width="100%">

|Runtime style change|Optimized performance through cache
|----------|-------
|<img alt="threebox" src="https://i.postimg.cc/QMh57yGP/Style-Change.gif" width="100%">|<img alt="threebox" src="https://i.postimg.cc/zf2wTYwB/Performance.gif" width="100%">

|Customizable FOV|Geojson and Points Extrusions
|---------|-------
|<img alt="threebox" src="https://i.postimg.cc/43Lh7vvR/Customizable-FOV.gif" width="100%">|<img alt="threebox" src="https://i.postimg.cc/50KqJdKv/extrusions.gif" width="100%">

|Sunlight illumination for a given datetime and lnglat|Models built-in shadows and sky layer synced with Sunlight
|---------|-------
|<img alt="threebox" src="https://i.postimg.cc/6QnjWSVm/Eiffel-Shadow.gif" width="100%">|<img alt="threebox" src="https://i.postimg.cc/63Y7SP6t/SunSki.gif" width="100%">

<br>



- - -


## Documentation
<img alt="threebox" src="docs/soldieranimation.jpg">

All the [**ThreeLibre Documentation**](/docs/Threebox.md) has been completely updated, including all the methods, properties and events implemented in Threebox and objects, but still *'work in progress'* adding better documented examples and images to illustrate Threebox capabilities.
- [**Using ThreeLibre**](/docs/Threebox.md#using-threebox)
- [**Loading a 3D Model**](/docs/Threebox.md#loading-a-3d-model)
- [**ThreeLibre methods**](/docs/Threebox.md#threebox-methods)
- [**Object methods**](/docs/Threebox.md#object-methods)
- [**Examples**](/examples/README.md)

<br>

- - -

## Compatibility/Dependencies

- [**Three.js 132**](https://github.com/mrdoob/three.js/releases/tag/r132). (already bundled into the Threebox build). If desired, other versions can be swapped in and rebuilt [here](https://github.com/jscastro76/threebox/blob/master/src/three.js), though compatibility is not guaranteed.
- **Maplibre-gl v4.1.3**. 
- **Azure Maps v2.0.31.**

<br>

- - -

## Getting started

You can use threelibre in three different ways. 

#### NPM install
Add threelibre to your project via **npm package**
```js
npm install threelibre-plugin
```   

Then you will need to import Threebox object in your code. Depending your javascript framework this might be different. 
```js 
import { Threebox } from 'threelibre-plugin'; 
```  
Depending the framework, wrapper or bundler you ar using, try with this:
```js 
import { Threebox } from 'threelibre-plugin/dist/threebox'; 
```  

<br/>

#### Use the bundle locally
Download the bundle from [`dist/threebox.js`](dist/threebox.js) or [`dist/threebox.min.js`](dist/threebox.min.js) and include it in a `<script>` tag on your page.  
If you want to use styles predefined, add the link to the cascade style sheet, just ensure the `src` and `href` attributes are pointing to relative or absolute url path.  
```html
<script src="../dist/threebox.js" type="text/javascript"></script>
<link href="../dist/threebox.css" rel="stylesheet" />
```
<br/>

#### Public CDNs
Threebox can be also used from different public CDNs:

<br/>

##### unpkg
Despite this CDN admits version, if omitted, it will download always the last one published.

```html
<script src="https://unpkg.com/threelibre-plugin/dist/threebox.min.js" type="text/javascript"></script>
<link href="https://unpkg.com/threelibre-plugin/dist/threebox.css" rel="stylesheet" />
```

For an specific version (i.e. v0.0.1) use the followin:
```html
<script src="https://unpkg.com/threelibre-plugin@0.0.1/dist/threebox.min.js" type="text/javascript"></script>
<link href="https://unpkg.com/threelibre-plugin@0.0.1/dist/threebox.css" rel="stylesheet" />
```

<br/>

#### Test the samples 
Several introductory examples are [here](https://github.com/piemonSong/threelibre/tree/master/examples).  
To run them, create a `config.js` file with your Mapbox-gl-js access token, alongside and in the format of [the template](https://github.com/piemonSong/threelibre/blob/master/examples/config_template.js).

<br>

- - -

## Contributing
- Clone the [Github repo](https://github.com/jscastro76/threebox/).
- Build the library with `npm run build` to get the minimized version, or `npm run dev` to get the development version and rebuild continuously as you develop. 
- Both commands will output a bundle in [`dist/`](dist/) folder.

#### Unit tests
Tests live [here](/tests). 
- Build first the test bundle with `npm run test`, this will create [`tests\threebox-tests-bundle.js`](tests/threebox-tests-bundle.js)  
- Then in your preferred browser navigate to [`threebox-tests.html`](https://github.com/jscastro76/threebox/blob/master/tests/threebox-tests.html) and check the console for test results.

#### How to build the project in Visual Studio
Sample to get a full build from scratch for Visual Studio:
- Install [Node.js](https://nodejs.org/en/) 
- Clone the repo and open a new Project using main.js
- Install / Update the packages browserify, tape, ncp, uglyfy, watchify.
- Right click on the project at the Solution Explorer > Open Node.js Interactive Window:
- execute `.npm [ProjectName] init -y`
- execute `.npm [ProjectName] install`
- execute `.npm [ProjectName] i`
- execute `.npm [ProjectName] run dev` or `.npm run build
`


