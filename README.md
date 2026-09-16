# Ocean Wave Energy Mapper

A classical computer vision project that visualizes accumulated motion 
intensity in ocean wave footage, highlighting zones of highest wave 
activity over time — a lightweight approach inspired by real-world 
coastal monitoring techniques used to flag potentially hazardous areas 
(e.g., rip currents).

![Sample Output](sample_output.gif)

## How It Works

The pipeline processes the video frame-by-frame:

1. **Frame Differencing** — compares each frame to the previous one to detect motion
2. **Thresholding** — filters out minor noise, keeping only meaningful motion
3. **Accumulation** — builds up a motion-intensity map across the entire video
4. **Normalization & Color Mapping** — converts accumulated values into a visual heatmap
5. **Blending** — overlays the heatmap on the original footage
6. **Contour Detection** — identifies and flags the region with the highest wave activity

## Technologies
Python | OpenCV | NumPy

## Limitations
- Motion intensity reflects visual change, not actual wave height or water depth — it's a visual approximation, not a physical measurement
- Designed for fixed-camera footage; camera movement would introduce false motion readings
- Threshold values were tuned for this specific footage and may need adjustment for different lighting/wave conditions

## Video Source
[Mixkit — Free Stock Video](https://mixkit.co) (Free License)
