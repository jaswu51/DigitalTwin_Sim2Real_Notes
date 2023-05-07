
### future plan
* literature review, the state-of-art vision perception and sim2real research, eg. following up ICRA 2023
* redo the pipeline, may alter the scene and modify the reward function; and instead of using Mujoco, try to use Isaac Sim
* upgrade the task, from route planning to grasping, which requires **nerf segmentation**
* try to speed up the nerf process, like **real-time nerf** or **instant nerf**, to make it useful in daily life

### timeline
June -- pipeline running smoothly

mid August -- report submitting deadline

early September -- master thesis defense

# DigitalTwin_StudyNotes

### RGBD VS LIDAR
The functional difference between LiDAR and other forms of ToF is that LiDAR uses pulsed lasers to build a point cloud, which is then used to construct a 3D map or image. ToF applications create "depth maps" based on light detection, usually through a standard RGB camera.

### COLMAP and NERF
COLMAP and NERF can be used together in a pipeline for generating photorealistic 3D reconstructions of scenes from a series of 2D images. Here is an example pipeline:

* Capture a series of 2D images of the scene using a camera or cameras.

* Use COLMAP to generate a 3D model of the scene from the set of images, using techniques such as structure-from-motion (SfM) and multi-view stereo (MVS).

* Use the 3D model generated by COLMAP as input to NERF to generate photorealistic images of the scene from novel viewpoints.

* Optionally, refine the 3D model generated by COLMAP using the photorealistic images generated by NERF.

# Nerf Experiments
* Fork https://github.com/NVlabs/instant-ngp
* Create your own folder that containts the video, i.e. jas folder that contains jas.mp4
* cd jas folder
* run the following commands:
```
 C:\Users\jasmi\Documents\GitHub\instant-ngp\scripts\colmap2nerf.py  --run_colmap --aabb_scale 64 --overwrite
 python ..\scripts\colmap2nerf.py --video_in jas.mp4 --video_fps 10 --run_colmap --overwrite
```
* drag processed jas folder into the instant-ngp.exe from "Nerf_experiments\Instant-NGP-for-RTX-3000-and-4000\Instant-NGP-for-RTX-3000-and-4000\instant-ngp.exe"
