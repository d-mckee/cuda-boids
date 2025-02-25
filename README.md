﻿# cuda-boids

A quick experiment in OpenGL / CUDA interop, using the boids steering model as a focus. Boids are drawn as single points and rendered from device memory. A buffer for boid objects is created with OpenGL, registered with CUDA, and then the CUDA kernel moves each boid by accessing that buffer memory directly, requiring no transfer between host and device memory.

https://user-images.githubusercontent.com/36770835/164177978-1a9e5058-2819-4682-bcb8-5e75c603ca94.mp4

Boids are colored according to their heading (X component mapped to R channel, Y component mapped to G channel, Z component mapped to B channel), allowing for a primitive visualization of groupings. The movement rules followed by each boid can be weighted by constants in the program, and affect the overall order of the system.
