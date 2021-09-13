---
title: "three.js"
alias: "three.js"
tags: 
---

[index](/.md) < [programming](1-programming.md) < [creative code](creative-code.md)

(note, this is actually for me, so the writing is very specific.)

## what is three.js?
a javascript library (by mr.doob) used to create, display, and manipulate 3d objects in the web browser.

## how do you use it?
there are a few ways, but i think the simplest method for me right now is to use [npm.](npm.md)
- create a new project folder, nativate to it in vs, and open terminal (ctrl+j). to install the three npm module, run:
	``` 
	import * as THREE from 'three';
	```
- you'll need a bundling tool like [webpack](https://webpack.js.org/) as well (puts together your JavaScript, HTML, CSS, etc. files in a nice package). for example, you'll need the index.html file, the canvas.js file, the css file, etc.

	- side notes: rollup for bundling. tree shaking: removing dead code, which webpack can do automatically.
- however, you'll often need to import other features, such as controls, loaders, post-processing effects. these must be imported from examples/jsm.

### here's how to use three.js with static hosting (hugo)
in index.html, within the head
``` 
	<script type = "module">

	import * as THREE from 'https://cdn.skypack.dev/three@latest';
	const scene = new THREE.Scene();
	</script>
	
```

and to install examples, within the 'module'
```	
import { OrbitControls } from 
'https://cdn.skypack.dev/three@<version>/examples/jsm/controls/OrbitControls.js'; 

const controls = new OrbitControls();
```
## what do examples mean?
this refers to the other components that you can use in three.js that aren't initially included in the three module. they're called examples because they *are* examples — they're meant to be customized. these features can be [controls, loaders, post-processing effects,](https://threejs.org/examples/) etc. some that you use frequently are OrbitControls, BloomPass. 
	 One cool one is the [ASCII](https://threejs.org/examples/#webgl_effects_ascii) effect. Another is [marchingcubes.](https://threejs.org/examples/#webgl_marchingcubes) [Panorama/cube.](https://threejs.org/examples/#webgl_panorama_cube)[points/billboards.](https://threejs.org/examples/#webgl_points_billboards) [postprocessing/afterimage.](https://threejs.org/examples/#webgl_postprocessing_afterimage)[godrays.](https://threejs.org/examples/#webgl_postprocessing_godrays)[halftone.](https://threejs.org/examples/#webgl_postprocessing_rgb_halftone)[sobel.](https://threejs.org/examples/#webgl_postprocessing_sobel)

import them into 'module',

``` import { OrbitControls } from 
'three/examples/jsm/OrbitControls.js' 

const controls = new OrbitControls();
```

## what do you need in a scene?
## how do you make objects move?
## cameras
## how do you fix resizing issues?
## what types of geometries are in three.js?
## what's an easy way to adjust properties in realtime?
## how do you load textures?
- types of textures
- how to load
- uv unwrapping
- things you can do 
	- rotation, offset, repeat wrapping
- mipmapping and filtering
	- minification filter
		- THREE.NearestFilter best for performance
			- 
		- moire patterns
	- magnification filter
- performance
	- weight
		- prefer .jpg, and can use tinypng
	- size
		- reduce as much as possible, and wxh must be a power of 2 (512, 1024, 2048)
	- data
		- normal textures should be png

## materials
- normals: 

creative dev, designer, digital artist


new THREE.UpperCase
- material.envMap has to be before dat.gui


## lights
1. how to optimize performance
	1. Minimal cost:
-   AmbientLight
-   HemisphereLight
Moderate cost:
-   DirectionalLight
-   PointLight
High cost:
-   SpotLight
-   RectAreaLight

you can also bake light directly into the material via uv unwrapping