# Naive_Wiggle_Stereoscopy_Gifs
### Project Description
The original scope of the project was to recreate the results in the paper “Kinetic Depth Images: Flexible Generation of
Depth Perception”. In it, the researchers expand on the concept of wiggle stereoscopy by creating smooth transitions
between the two stereoscopic images rather than jumping between images. They do this by producing a depth map of
the scene from the two stereoscopic images and transforming the images to render intermediate frames between the
locations of the two images. In addition, to this, they try to maximize the perceived 3D effect of the gif by calculating an
energy map for the image using depth, inverted saliency, and centrality. Using this energy map, a pivot axis is
established which enhances the perceived 3D effect. I intended to recreate these elements to produce my own smooth
3D wiggle gifs.

It became clear almost immediately that the scope of the project would have to be reduced as soon as I set out
to code and implement the different elements of the KDI paper. The main issue was that there was very little
guidance or explanation behind the calculations for saliency and the depth mesh. The paper also briefly named
the method for producing intermediate frames without providing resources or explaining the method. Overall it
was infeasible to implement all the elements that went into the paper under those circumstances.

Rather than attempting to implement all the aspects of the paper, I decided to approach the project holistically. I
needed to produce a gif that would smoothly transition between the stereoscopic images. To do this, I needed to
produce the intermediate frames. I focused my attention only on implementing the concepts and methods in the
paper that would directly aid in producing these frames. Thus, I limited the scope of the project to generating
depth maps and constructing the transport maps that generated those frames.

### Inputs:
- Two stereoscopic images are required. These images both need to be taken with the same camera settings
pointed level at a target in focus at equal elevation. The first image is from the left perspective while the second image
is taken from the right perspective.
- Angle between left and right camera
- Angle of intermediate frame being generated Field of View
- Distance Factor

### Outputs: 
- a gif

If you are experiencing trouble viewing the script use: https://nbviewer.jupyter.org/
