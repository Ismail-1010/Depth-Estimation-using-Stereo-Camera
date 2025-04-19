
# 📌 Depth Estimation using Stereo Camera (ESP32-CAM)
This project demonstrates a cost-effective depth estimation system using a stereo vision setup built with two ESP32-CAM modules. Developed during my internship at SPARK MINDA Centre of Excellence in Automotive Electronics, REVA University, the system captures synchronized stereo images and computes depth maps using OpenCV.

🎯 Project Objectives

    -- Build a stereo camera system for real-time depth estimation.

    -- Use low-cost ESP32-CAM modules for live video transmission.

    -- Implement stereo image calibration,  disparity mapping, and object detection.

    -- Develop a scalable and affordable alternative to expensive depth cameras like Intel RealSense or OAK-D.

🛠️ Tools & Technologies

    -- ESP32-CAM

    -- OpenCV (Python)

    -- Arduino IDE

    -- Stereo Vision and Calibration Techniques

    -- Wi-Fi-based image streaming

🚘 Applications

    -- Obstacle detection and avoidance

    -- Smart parking systems

    -- Autonomous navigation

    -- Robotics and educational tools




📘 Stereo_Calibration.py
Purpose:

  -- This script performs stereo camera calibration using image pairs to compute depth-related parameters like focal length and angle of convergence (θ). These calibrated values are critical for accurate disparity calculation and 3D depth estimation in our stereo vision system.

Highlights:

  -- Uses object detection and segmentation with Mask R-CNN to localize targets in both images.

  -- Computes horizontal disparities between bounding boxes.

  -- Derives focal length and geometric configuration from known object distances.

  -- Outputs key calibration parameters: focal length (f) and tan(θ).

📘 Depth_Estimation.py

Purpose:

   -- This is the main inference script that connects to two ESP32-CAM modules, captures live stereo video streams, and performs real-time depth estimation and object detection.

Highlights:

   -- Streams video from ESP32-CAMs via IP.

   -- Performs Mask R-CNN–based detection on both left and right frames.

   -- Calculates disparity and applies calibrated geometry to estimate object distances.

   -- Annotates each object with its category and real-time distance in centimeters.

   -- Interactive controls to adjust resolution, quality, and white balance dynamically.

