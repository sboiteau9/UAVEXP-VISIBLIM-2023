# Documentation of "Experimental Data from Framework for Autonomous UAV Navigation and Target Detection in GPS-Denied and Visually Degraded Environments"

This is a repository which hosts the data collected during the below mentionned research paper:

Boiteau, Sebastien and Vanegas, Fernando and Gonzalez, Felipe, 2023, "Framework for Autonomous UAV Navigation and Target Detection in GPS-Denied and Visually Degraded Environments", ADD DOI.

## Overview about the data

This repository consists of two types of data. Firstly, it includes CSV files, which records several parameters such as the time step duration, UAV pose estimation, target position, actions....
Secondly, it contains rosbag containing the following variables: occupancy map, UAV pose, belief state of UAV position, belief state of Target position, and the YOLOv5 detection output. The YOLOv5 output does not contain the images but the actual detection output with the detected object's classe and bounding box coordinate. 
The data is first seperated by simulation and real-life testing, and then by map and visibility condition, as highlited below. 

**Real-Life Testing **

3.5 ON: map containing only 3.5 meters obstacles in normal visibility condition (lights ON).

3.5 OFF: map containing only 3.5 meters obstacles in low visibility condition (lights OFF).

DIFF ON: map containing 1.7 meters and 3.5 meters obstacles in normal visibility condition (lights ON).

DIFF OFF: map containing 1.7 meters and 3.5 meters in low visibility condition (lights OFF).

Picture bag: A folder containing short rosbags showing yolov5 detection images with the thermal camera during flight tests and on the ground to compare mannequin heat signature and human heat signature.


**Simulation**

3_5_Obst_LV: map containing only 3.5 meters obstacles in low visibility condition (smoke).

3_5_Obst_NV: map containing only 3.5 meters obstacles in normal visibility condition (no smoke).

Diff_Obst_LV: map containing 1.7 meters and 3.5 meters obstacles in low visibility condition (smoke).

Diff_Obst_NV: map containing 1.7 meters and 3.5 meters obstacles in normal visibility condition (no smoke).


The data is stored in csv files and rosbags.

### File and directory structure

```
├── REAL LIFE TESTING                    
    └── 3_5_OFF
        └── csv
        └── rosbag
    └── 3_5_ON
        └── csv
        └── rosbag
    └── DIFF_OFF
        └── csv
        └── rosbag
    └── DIFF_ON
        └── csv
        └── rosbag
    └── Pictures bag
├── SIMULATION
    └── 3_5_Obst_LV
        └── csv
        └── rosbag
    └── 3_5_Obst_NV
        └── csv
        └── rosbag
    └── Diff_Obst_LV
        └── csv
        └── rosbag
    └── Diff_Obst_NV
        └── csv
      
```
