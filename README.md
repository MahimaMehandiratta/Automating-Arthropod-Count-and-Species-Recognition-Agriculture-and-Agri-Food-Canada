# Automating-Arthropod-Count-and-Species-Recognition-Agriculture-and-Agri-Food-Canada
Developed an application for automating the count and species recognition of arthropods on sticky cards, utilizing image recognition technology in Roboflow and trained the model using Machine Learning algorithms such as Yolov8x and Faster R-CNN.

**Introduction**

This project represents a significant leap forward in agricultural monitoring techniques, harnessing advanced image recognition algorithms to identify and count various arthropod species captured on sticky cards. The project's primary goal was to automate the labor-intensive and error-prone process of manual counting and identification, providing a much-needed solution for the agricultural industry.

**Background and Objectives**

Background
In agricultural management, arthropods play a pivotal role in the vitality and productivity of ecosystems. Monitoring these species is essential for sustainable agricultural practices and effective pest control. Traditionally, sticky cards are used to trap various arthropod species, but counting and identifying these species manually is laborious and prone to error.
Objectives
The objective of this project was to develop an automated application that could swiftly recognize and enumerate six targeted arthropod classes from images of sticky cards. These classes are:
- Western flower thrips
- Orius insidiosus
- Nesidiocoris tenuis
- Whitefly (greenhouse)
- Melon aphid (winged)
- Two-spotted spider mite

**Methodology**

Leveraging RoboFlow
RoboFlow was chosen for its adeptness in handling the complexities of our dataset, providing an all-in-one solution for image preprocessing, annotation, and management. This platform streamlined our workflow, ensuring uniformity and precision in our dataset.
Steps:
- Image Acquisition & Conversion: High-resolution images (3000x3000 pixels) were resized to 640x640 pixels for the YOLOv8 neural network.
- Image Preprocessing: Cropping, normalization, and augmentation techniques were used to enhance image quality.
- Image Labeling & Dataset Insights: Manual annotation of arthropod instances using RoboFlow's interface.
- Centralizing Data: Consolidating labeled images into a unified dataset.
- Dataset Partitioning: Dividing the dataset into training, validation, and testing subsets.

**Models Used**

YOLOv8 Variants

YOLOv8x:
- High precision, suitable for detailed analysis but computationally intensive.
- Best for accuracy, slower inference time.
  
YOLOv8n:
- Fastest model, lower precision, ideal for real-time applications.
- Best for speed, lower accuracy.

YOLOv8-P2:
- Balanced precision and recall, suitable for detecting small objects.
- Middle ground between precision and speed.
 
Integration and Optimization:
- Hybrid approach combining YOLOv8n and YOLOv8-P2 for enhanced versatility and performance.

**Comprehensive Workflow Integration**

Training and Model Configuration (SAHI.ipynb):
- Configuring and training YOLOv8 models.
- Validating models against a separate test set.
  
Detection and Counting Script (app_NMS_SAHI.py):
- Detecting arthropods on new images.
- Logging detailed detection results.
  
Application Deployment (streamlit.ipynb):
- User-friendly GUI for uploading images and receiving detection results in real-time.

**Outcomes and Insights**
- Increased Efficiency: Automated monitoring reduced the time and effort required for manual observation.
- Accuracy and Consistency: Provided precise counts and species identifications, minimizing human error.
- Valuable Insights: Generated rich, reliable data for ecological studies and pest management strategies.

**Challenges**

- Computational Power: Limited GPU resources required algorithm optimization and scaling.
- Algorithm Refinement: Addressing class imbalance and improving feature extraction for diverse arthropod species.

**Lessons Learned**
- Continuous Refinement: Importance of iterative improvement for algorithm precision.
- Understanding Needs: Aligning project goals with agricultural sector requirements.
- Data Management: Ensuring robust data management for reliable machine learning.
- Tool Integration: Leveraging various tools for an optimal workflow.
- Algorithm Efficiency: Balancing precision with performance for real-world scenarios.
