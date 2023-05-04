# DigitalTwin_StudyNotes

### RGBD VS LIDAR
The functional difference between LiDAR and other forms of ToF is that LiDAR uses pulsed lasers to build a point cloud, which is then used to construct a 3D map or image. ToF applications create "depth maps" based on light detection, usually through a standard RGB camera.

### COLMAP and NERF
COLMAP and NERF can be used together in a pipeline for generating photorealistic 3D reconstructions of scenes from a series of 2D images. Here is an example pipeline:

* Capture a series of 2D images of the scene using a camera or cameras.

* Use COLMAP to generate a 3D model of the scene from the set of images, using techniques such as structure-from-motion (SfM) and multi-view stereo (MVS).

* Use the 3D model generated by COLMAP as input to NERF to generate photorealistic images of the scene from novel viewpoints.

* Optionally, refine the 3D model generated by COLMAP using the photorealistic images generated by NERF.

### philosophy question:

what is the point instead of feeding videos and train the computer vision network for route planning, but to represent everything in a virtual physical world? It makes sense that the collision between objects is important. But if the computer vision approach can cover almost every task, what is the point to build a virtual world?
