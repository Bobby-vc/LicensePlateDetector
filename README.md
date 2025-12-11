## **AUTOMATED LICENSE PLATE DETECTION SYSTEM**

This project builds a computer vision system that automatically detects vehicle license plates in images using a YOLOv8 object detection model. It is designed for parking management, security monitoring, tolling systems, and other environments where identifying vehicles quickly and accurately is essential.

Demo Video: https://drive.google.com/file/d/1_2oUbkpl4zjI9Q5_x6hCD1SLmM-glbmR/view?usp=drive_link

Team Members: Akinbobola Akinpelu

Tier Selection: Tier 2 — Object Detection

I chose this because the project involves detecting a specific object class ("license_plate") using a pretrained YOLO model and a custom dataset.

1. Problem Statement

Organizations such as parking facilities, schools, apartments, and toll systems often rely on manual entry or visual inspection of vehicle plates.
This process is:
- Slow
- Error-prone
- Not scalable for real-time operations
- Manual license plate identification can also introduce inconsistencies in access control logs and delays in verification workflows.

2. Solution

This project implements an automated license plate detection pipeline using YOLOv8. The system will:
- Take images as input
- Detect and localize license plates with bounding boxes
- Output visual results + structured detection data
- Support real-time or batch-processing use cases

A fast and accurate YOLO-based system that detects license plates automatically from images.


3. Technical Approach

Technique: Object Detection

Model: YOLOv8n or YOLOv8s (Ultralytics)

Frameworks: PyTorch, Ultralytics YOLOv8

Why YOLOv8? 
- State-of-the-art accuracy on small objects like license plates
- Fast inference suitable for real-time deployment
- Lightweight and easy to fine-tune on custom datasets
  
4. Dataset Plan

Source: Roboflow — Vehicle Registration Plates dataset https://universe.roboflow.com/augmented-startups/vehicle-registration-plates-trudk/dataset/1

Size: ~300–1,000 images

Labels: "license_plate"

Format: YOLOv5/YOLOv8 compatible

Actions:

- Validate folder structire after unzipping
- Clean dataset folders
- Ensure data.yaml path is correct
- Split into train/val/test
- Apply augmentations

5. Metric Targets

mAP50	≥ 0.85

Precision	≥ 0.90

Latency	< 0.05 seconds/image

6. Week-by-Week Timeline

Week 10 - Collect dataset + set up environment

Week 11 - Train YOLOv8 model on Roboflow dataset

Week 12	- Test + improve performance

Week 13	- Build end-to-end demo notebook

Week 14 -	Write documentation + finalize repo

Week 15 -	Present project

7. Risks & Mitigation
- Dataset path issues in Colab | High Probability | Manually define absolute paths
- Not enough data | Medium Probability | Add augmentation
- Training runtime too long | Medium Probability | Use YOLOv8n 
- Model underperforms in low-light images | Medium Probability | Apply brightness
