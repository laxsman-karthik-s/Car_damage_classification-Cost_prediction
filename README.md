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
## Results
The performance of the Car Damage Classification and Cost Prediction System, which consists of four modules, was evaluated using the RCNN (Region Convolutional Neural Network) model. The modules and their corresponding performance are discussed below:
Modules Overview:
1.	Car Detection (Module 1): Determines if the object in the image is a car.
2.	Damage Detection (Module 2): Classifies whether the car is damaged or not.
3.	Damage Severity Classification (Module 3): Determines the severity of the damage (e.g., minor, moderate, severe).
4.	Damage Location Identification (Module 4): Identifies the specific region of the car (front, side, rear) affected by the damage.
RCNN Model Performance:
1.	Car Detection (Module 1):
- Accuracy: 
The RCNN model performed well in detecting whether the object in the image was a car or not. It accurately identified cars in a variety of settings, despite challenges such as varying lighting conditions, background complexity, and different car models.
 
2.	Damage Detection (Module 2):
- Accuracy: 
The damage detection module performed with good accuracy, identifying whether a car was damaged or undamaged. However, some false positives were detected where undamaged cars were incorrectly classified as damaged, likely due to environmental factors (e.g., reflective surfaces or minor scratches).
 
3.	Damage Severity Classification (Module 3):
- Accuracy: 
The severity classification module struggled in some cases to distinguish between minor and moderate damage, particularly for less obvious or smaller damages. It performed well in distinguishing severe damage, as the model was able to identify significant damage areas with higher confidence.
 
4.	Damage Location Identification (Module 4):
- Accuracy: 
The location identification module, which uses RCNN to detect specific regions of the car (e.g., front, side, or rear), had the lowest accuracy among the four modules. This may be due to complex shapes or overlapping areas of damage, which made it difficult for the model to distinguish exact locations accurately.

Results of Model comparison :
A comparison of model performance metrics reveals the effectiveness of RCNN and YOLO in the Car Damage Classification and Cost Prediction system. With a training accuracy of 60.08%, RCNN outperformed YOLO, which achieved a training accuracy of 43%. Both models were assessed on their ability to detect car damage, classify its severity, and identify damage locations, with RCNN consistently providing better results. 
 
Model Performance Analysis
1.	RCNN Performance:
o	RCNN demonstrated superior accuracy compared to YOLO, especially in detecting subtle damages and correctly classifying severity levels.
o	The region-based analysis enabled RCNN to provide detailed spatial insights into damage locations, making it highly reliable for detailed assessments required in insurance and repair cost prediction.
2.	YOLO Performance:
o	While YOLO's speed and efficiency made it suitable for real-time applications, its overall accuracy was lower due to its grid-based approach, which occasionally missed finer details in damage patterns.
o	Despite this, YOLO excelled in providing rapid assessments, which can be useful in scenarios demanding quick decisions.
The results highlight RCNN’s effectiveness in achieving higher accuracy, making it the preferred model for detailed damage analysis and cost prediction. YOLO, while not as precise, offers unparalleled speed and efficiency, making it valuable for real-time applications such as preliminary assessments or field-based evaluations.
The stark contrast in accuracy underscores the trade-off between precision and speed in model selection:
o	RCNN is ideal for use cases demanding thorough analysis and accuracy, such as generating insurance reports or repair estimates.
o	YOLO is suitable for scenarios where rapid assessments are prioritized, such as initial damage scans or customer-facing applications.
These findings offer stakeholders clear insights into the applicability of each model and guide their selection based on specific use-case requirements.

## Conclusion
The Car Damage Classification and Cost Prediction System developed in this project leverages advanced RCNN (Region Convolutional Neural Network) techniques to effectively identify car damages and estimate repair costs. The system consists of four main modules: car detection, damage detection, severity classification, and damage location identification. While the car and damage detection modules achieved impressive accuracies of 85.47% and 83.20%, respectively, the damage location identification module faced challenges, reaching only 60.08% due to overlapping damage areas and complex car shapes. RCNN proved to be superior to other models like YOLO, particularly for detailed object localization and severity estimation. Additionally, the integrated cost prediction feature, based on damage severity and location, provides valuable insights for real-time assessments in insurance and repair contexts. Overall, this project highlights the promising role of deep learning and computer vision in car damage assessment, though further enhancements in image resolution and training data could improve accuracy, especially in more complex tasks.
## Sample Output
![html](https://github.com/user-attachments/assets/563c7bec-ffb8-4b95-b200-2a35a87266f0)
![html2](https://github.com/user-attachments/assets/401d8146-e597-44d5-b9e8-d27157bb7144)
