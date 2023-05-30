
### future plan
* extract the mesh from nerf to blender/mujoco/isaac sim. https://www.youtube.com/watch?v=55XKtYOIB7Y (Done)
* literature review, the state-of-art vision perception and sim2real research, eg. following up ICRA 2023
* redo the pipeline, may alter the scene and modify the reward function; and instead of using Mujoco, try to use Isaac Sim
* upgrade the task, from route planning to grasping, which requires **nerf segmentation**
* try to speed up the nerf process, like **real-time nerf** or **instant nerf**, to make it useful in daily life

### timeline
mid June -- pipeline running smoothly

mid August -- report submitting deadline

early September -- master thesis defense


# Isaac Gym

IsaacGymEnvs （IGE）

https://github.com/NVIDIA-Omniverse/IsaacGymEnvs

omni.isaac.gym （OIG）

https://github.com/NVIDIA-Omniverse/OmniIsaacGymEnvs

https://docs.omniverse.nvidia.com/app_isaacsim/app_isaacsim/tutorial_gym_isaac_gym.html

reference: [zhihu](https://www.zhihu.com/search?type=content&q=omni.isaac.gym)

# Custom RL Example using Stable Baselines
https://docs.omniverse.nvidia.com/app_isaacsim/app_isaacsim/tutorial_gym_new_rl_example.html


# DigitalTwin_StudyNotes

### RGBD VS LIDAR
The functional difference between LiDAR and other forms of ToF is that LiDAR uses pulsed lasers to build a point cloud, which is then used to construct a 3D map or image. ToF applications create "depth maps" based on light detection, usually through a standard RGB camera.

### COLMAP and NERF

COLMAP and NeRF are two different approaches used in computer vision and graphics, with different purposes and methodologies. Here's a brief explanation of each:

* COLMAP (Structure from Motion):
COLMAP is a software package that focuses on structure from motion (SFM) and multi-view stereo (MVS). It is primarily used for 3D reconstruction of scenes or objects from a collection of 2D images. COLMAP utilizes feature extraction, matching, camera pose estimation, and triangulation techniques to generate a 3D model from a set of images. It can be used for applications such as creating 3D models of environments, objects, or even for augmented reality.

* NeRF (Neural Radiance Fields):
NeRF is a deep learning-based technique used for synthesizing novel views of a scene or object. It models the scene as a continuous 3D function called a neural radiance field. NeRF learns to predict the appearance (color and intensity) of a scene from any given viewpoint by training on a dataset of images with corresponding camera poses. NeRF can generate photo-realistic renderings of scenes, even from viewpoints not present in the original dataset. It is commonly used for applications such as virtual reality, computer graphics, and generating synthetic images.

In summary, COLMAP focuses on reconstructing 3D geometry from images, while NeRF focuses on synthesizing novel views of a scene or object using a neural network-based approach.

COLMAP and NERF can be used together in a pipeline for generating photorealistic 3D reconstructions of scenes from a series of 2D images. Here is an example pipeline:

* Capture a series of 2D images of the scene using a camera or cameras.

* Use COLMAP to generate a 3D model of the scene from the set of images, using techniques such as structure-from-motion (SfM) and multi-view stereo (MVS).

* Use the 3D model generated by COLMAP as input to NERF to generate photorealistic images of the scene from novel viewpoints.

* Optionally, refine the 3D model generated by COLMAP using the photorealistic images generated by NERF.

###  Nerf Inputs

The NeRF (Neural Radiance Fields) paper, titled "NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis," introduces a novel approach for synthesizing novel views of a scene. The inputs to the NeRF algorithm described in the paper are as follows:

* Dataset of Images:
The algorithm requires a dataset of images captured from various viewpoints of the scene or object of interest. The images should cover different angles, positions, and perspectives to provide a diverse set of views.

* Camera Poses:
For each image in the dataset, corresponding camera poses are needed. Camera poses define the position and orientation of the camera when capturing the image. These poses are typically represented by a combination of rotation and translation matrices or other suitable representations.

* Calibration:
Calibration information is necessary to account for any camera-specific parameters such as intrinsic camera parameters (focal length, principal point) and distortion coefficients. Calibration ensures accurate mapping between the 3D scene and the 2D images.

* Camera Parameters:
Additional camera parameters may be required, such as exposure settings (shutter speed, aperture) and sensor-specific information, depending on the specific implementation or variations of the NeRF algorithm.

These inputs are used during the training phase of the NeRF algorithm to learn a neural network model that can predict the appearance of the scene from any given viewpoint. By training on the dataset of images and corresponding camera poses, NeRF learns to model the scene as a continuous 3D function called a neural radiance field, allowing it to synthesize realistic images from novel viewpoints.

referencce: https://www.bilibili.com/video/BV1d34y1n7fn/?spm_id_from=333.337.search-card.all.click&vd_source=9def8c0da178e13205a9ab695cc12d7c

### Domain randomization
Domain randomization is a technique used in robotics and machine learning to improve the robustness and adaptability of robots in real-world environments. It involves systematically randomizing various aspects of the training process, including the simulation environment, object appearances, lighting conditions, physics parameters, and other factors, to create a diverse set of training data.

The goal of domain randomization is to expose the robot to a wide range of possible scenarios during training so that it learns to generalize its behavior and can handle unforeseen situations in the real world. 
# Isaac Sim tutorials
import URDF
https://www.youtube.com/watch?v=pxPFr58gHmQ

# Robot Library
https://robodk.com/library

# Ros2 tutorial
https://docs.ros.org/en/eloquent/Tutorials/Writing-A-Simple-Py-Service-And-Client.html#pysrvcli

build a robot from urdf and meshes

https://automaticaddison.com/how-to-create-a-simulated-mobile-robot-in-ros-2-using-urdf/
