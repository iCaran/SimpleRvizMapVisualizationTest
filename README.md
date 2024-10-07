# Simple Rviz Map-Visualization Test    

This is a minimal ROS 2 package that publishes a simple occupancy grid to reproduce an issue with RViz on the Raspberry Pi.

## How to Run

1. Clone the repository into your ROS workspace:
   ```bash
   git clone https://github.com/iCaran/SimpleRvizMapVisualizationTest.git
   ```
2. Build the workspace:
   ```bash
   colcon build
   source install/setup.bash
   ```
3. Run the node:
   ```bash
   ros2 run simple_map_test simple_map_publisher
   ```
4. Visualize the `/map` topic in RViz.

## Issue

The following error is encountered in RViz:

```
[INFO] [1728230864.027825491] [rviz2]: Stereo is NOT SUPPORTED 
[INFO] [1728230864.027933543] [rviz2]: OpenGl version: 3.1 (GLSL 1.4) 
[INFO] [1728230864.075937684] [rviz2]: Stereo is NOT SUPPORTED 
[ERROR] [1728230881.860686592] [rviz2]: rviz/glsl120/indexed_8bit_image.vert rviz/glsl120/indexed_8bit_image.frag
 GLSL link result: 
active samplers with a different type refer to the same texture image unit
```
