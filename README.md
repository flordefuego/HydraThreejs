# HydraThreejs
Temporary solution for using Threejs in Hydra

```
await loadScript("https://unpkg.com/three@0.97.0/build/three.js") //just replace the original example with this URL

scene = new THREE.Scene()
camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000)

renderer = new THREE.WebGLRenderer()
renderer.setSize(width, height)
geometry = new THREE.BoxGeometry()
material = new THREE.MeshBasicMaterial({color: 0x00ff00})
cube = new THREE.Mesh(geometry, material);
scene.add(cube)
camera.position.z = 1.5

// 'update' is a reserved function that will be run every time the main hydra rendering context is updated
update = () => {
  cube.rotation.x += 0.01;
  cube.rotation.y += 0.01;
  renderer.render( scene, camera );
}

s0.init({ src: renderer.domElement })

src(s0).repeat().out()
```

## Try Hydra scketch [Here](https://hydra.ojack.xyz/?code=YXdhaXQlMjBsb2FkU2NyaXB0KCUyMmh0dHBzJTNBJTJGJTJGdW5wa2cuY29tJTJGdGhyZWUlNDAwLjk3LjAlMkZidWlsZCUyRnRocmVlLmpzJTIyKSUwQSUwQXNjZW5lJTIwJTNEJTIwbmV3JTIwVEhSRUUuU2NlbmUoKSUwQWNhbWVyYSUyMCUzRCUyMG5ldyUyMFRIUkVFLlBlcnNwZWN0aXZlQ2FtZXJhKDc1JTJDJTIwd2luZG93LmlubmVyV2lkdGglMjAlMkYlMjB3aW5kb3cuaW5uZXJIZWlnaHQlMkMlMjAwLjElMkMlMjAxMDAwKSUwQSUwQXJlbmRlcmVyJTIwJTNEJTIwbmV3JTIwVEhSRUUuV2ViR0xSZW5kZXJlcigpJTBBcmVuZGVyZXIuc2V0U2l6ZSh3aWR0aCUyQyUyMGhlaWdodCklMEFnZW9tZXRyeSUyMCUzRCUyMG5ldyUyMFRIUkVFLkJveEdlb21ldHJ5KCklMEFtYXRlcmlhbCUyMCUzRCUyMG5ldyUyMFRIUkVFLk1lc2hCYXNpY01hdGVyaWFsKCU3QmNvbG9yJTNBJTIwMHgwMGZmMDAlN0QpJTBBY3ViZSUyMCUzRCUyMG5ldyUyMFRIUkVFLk1lc2goZ2VvbWV0cnklMkMlMjBtYXRlcmlhbCklM0IlMEFzY2VuZS5hZGQoY3ViZSklMEFjYW1lcmEucG9zaXRpb24ueiUyMCUzRCUyMDEuNSUwQSUwQSUyRiUyRiUyMCd1cGRhdGUnJTIwaXMlMjBhJTIwcmVzZXJ2ZWQlMjBmdW5jdGlvbiUyMHRoYXQlMjB3aWxsJTIwYmUlMjBydW4lMjBldmVyeSUyMHRpbWUlMjB0aGUlMjBtYWluJTIwaHlkcmElMjByZW5kZXJpbmclMjBjb250ZXh0JTIwaXMlMjB1cGRhdGVkJTBBdXBkYXRlJTIwJTNEJTIwKCklMjAlM0QlM0UlMjAlN0IlMEElMjAlMjBjdWJlLnJvdGF0aW9uLnglMjAlMkIlM0QlMjAwLjAxJTNCJTBBJTIwJTIwY3ViZS5yb3RhdGlvbi55JTIwJTJCJTNEJTIwMC4wMSUzQiUwQSUyMCUyMHJlbmRlcmVyLnJlbmRlciglMjBzY2VuZSUyQyUyMGNhbWVyYSUyMCklM0IlMEElN0QlMEElMEFzMC5pbml0KCU3QiUyMHNyYyUzQSUyMHJlbmRlcmVyLmRvbUVsZW1lbnQlMjAlN0QpJTBBJTBBc3JjKHMwKS5yZXBlYXQoKS5vdXQoKSUwQSUwQQ%3D%3D)
