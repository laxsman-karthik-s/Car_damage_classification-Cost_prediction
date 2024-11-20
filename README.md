# Car_damage_classification-Cost_prediction
Note: Read the instruction.md file carefully.
## Introduction
Assessing car damage for insurance claims has often been a slow and inconsistent process, relying heavily on manual inspections that can lead to human error. Our project aims to change that by using advanced deep learning technologies to automate the detection of car damage and estimate repair costs. By harnessing the power of sophisticated RCNN models and data-driven methods, we offer a more efficient and reliable alternative to traditional damage assessment.
## Dataset Description
For our project, we created a vast and varied dataset by combining web scraping with publicly available datasets. This approach allowed us to gather a comprehensive collection of car images that would be essential for training and validating our model.

Using Python-based web scraping tools, we collected around 200 images from various online sources. We made sure to include a wide range of car models, types of damage, and different environmental conditions. This effort was crucial to ensure that our dataset reflected real-world variations in lighting, angles, and the severity of damage.

In addition to our scraped images, we supplemented our dataset with existing collections from Kaggle, which is known for its extensive resources in data science. These datasets featured labelled images of cars, clearly indicating whether each vehicle was damaged or undamaged, along with detailed annotations about the severity and location of the damage (like the front bumper or rear panel).
## Proposed System
Our project introduces an advanced deep learning pipeline for automating car damage assessment and repair cost prediction. By leveraging the power of Region-based Convolutional Neural Networks (RCNN), this system efficiently classifies damage, determines its severity and location, and estimates repair costs, offering a complete solution for automotive insurance and repair workflows.
1. Data Preparation
- Web Scraping: Python-based web scraping tools were employed to gather thousands of car images from online platforms such as car repair websites and insurance claim portals. The dataset includes images of both damaged and undamaged cars, annotated with details about damage type, severity, and location.
- Dataset Augmentation: To ensure model robustness, data augmentation techniques such as flipping, rotation, cropping, and brightness adjustments were applied. These techniques simulate diverse environmental and photographic conditions, enriching the dataset's variability.
2. RCNN Architecture
-	Car Detection:
The first stage of the RCNN pipeline identifies and localizes cars in the images using bounding boxes. This ensures that only relevant areas of the image are processed in subsequent steps.
-	Damage Detection:
In the second stage, the model classifies the detected objects as damaged or undamaged. This binary classification filters out undamaged cars, optimizing processing efficiency.
-	Severity Classification:
The third stage focuses on categorizing the severity of damage into levels such as minor, moderate, or severe. This model leverages features like the size, shape, and intensity of the damage to deliver precise predictions.
-	Location Identification:
The final stage determines the specific region of the car affected by damage (e.g., front bumper, rear panel, side door). This spatial analysis provides a detailed overview of the damage, facilitating accurate cost estimation.
3. Cost Prediction Module
-	Integration with RCNN:
A regression model is integrated with the RCNN pipeline to predict repair costs based on predefined mappings between damage severity, location, and real-world repair costs derived from the dataset.
-	Output:
The module provides a numerical estimate of the repair cost, offering actionable insights for insurance claims and repair decisions.
## Conclusion
The Car Damage Classification and Cost Prediction System developed in this project leverages advanced RCNN (Region Convolutional Neural Network) techniques to effectively identify car damages and estimate repair costs. The system consists of four main modules: car detection, damage detection, severity classification, and damage location identification. While the car and damage detection modules achieved impressive accuracies of 85.47% and 83.20%, respectively, the damage location identification module faced challenges, reaching only 60.08% due to overlapping damage areas and complex car shapes. RCNN proved to be superior to other models like YOLO, particularly for detailed object localization and severity estimation. Additionally, the integrated cost prediction feature, based on damage severity and location, provides valuable insights for real-time assessments in insurance and repair contexts. Overall, this project highlights the promising role of deep learning and computer vision in car damage assessment, though further enhancements in image resolution and training data could improve accuracy, especially in more complex tasks.
## Sample Output
![html](https://github.com/user-attachments/assets/563c7bec-ffb8-4b95-b200-2a35a87266f0)
![html2](https://github.com/user-attachments/assets/401d8146-e597-44d5-b9e8-d27157bb7144)
