* Fork https://github.com/NVlabs/instant-ngp

* Put a short video into a folder, i.e. named ../jas/jas.mp4

* cd jas folder and run the following command to get the camera poses

```
 python ..\scripts\colmap2nerf.py --video_in jas.mp4 --video_fps 10 --run_colmap --overwrite
 ```

 * run Nerf_experiments/Instant-NGP-for-RTX-3000-and-4000/Instant-NGP-for-RTX-3000-and-4000/instant-ngp.exe

 * drag the processed jas folder into the program, you will see Nerf starts to render the sccene