# 🛒 SmartShelf AI — Intelligent Shelf Monitoring System

## 🌐 Live Demo

**Streamlit Application:**
(https://1000410harinipriyakarthikeyansmartshelfai-y4mjfjehgpqjbahifxct.streamlit.app/)

## 📌 1. Project Overview

SmartShelf AI is a computer vision project designed to explore how artificial intelligence can support automated shelf monitoring and product availability analysis.

Traditional shelf monitoring often requires people to inspect shelves manually, which can be time-consuming and may lead to missed stock shortages. Computer vision offers an alternative by analysing images and identifying products or shelf conditions automatically.

This project combines machine learning concepts with an interactive Streamlit application to demonstrate how AI can support inventory monitoring and retail decision-making.

## 🎯 2. Problem Statement

Manual shelf inspection can make it difficult to monitor product availability consistently, particularly in environments with many products and frequent stock changes.

The main objective of SmartShelf AI is to investigate how a computer vision model can identify relevant visual information from shelf images and present useful results through a web-based interface.

### Project Objectives

- Explore object detection for automated shelf monitoring.
- Prepare image data for model training and evaluation.
- Train and evaluate a suitable computer vision model.
- Analyse model performance using appropriate evaluation metrics.
- Develop an interactive application for demonstrating the model.
- Investigate how AI can improve the efficiency of inventory monitoring.

## 🔬 3. Research Background and Findings

Research in computer vision has demonstrated that deep learning can identify and localise objects in images. Object detection models predict the classes and locations of objects, making them useful for applications that require more than simple image classification.

The following research findings provide the theoretical background for this project.

### 3.1 Deep Learning for Object Detection

Convolutional neural networks learn visual features from image data. These features can help a model distinguish between objects based on their appearance, shape, and surrounding visual information.

**Relevance to the project:** A trained object detection model can potentially identify products or other relevant objects in shelf images.

### 3.2 YOLO-Based Object Detection

The You Only Look Once (YOLO) approach performs object detection in a single network evaluation, enabling efficient predictions. Modern YOLO implementations are widely used in real-time computer vision applications.

**Relevance to the project:** A YOLO-based model is a suitable candidate when both object localisation and reasonably fast inference are required.

### 3.3 Dataset Quality and Generalisation

A model's performance depends on the quality, quantity, diversity, and labelling accuracy of its training data. Evaluation on data not used for training helps estimate how well the model generalises to unseen examples.

**Relevance to the project:** Careful data preparation and separate training, validation, and testing datasets are important for reliable evaluation.

### 3.4 Research Summary

The research background suggests that an effective shelf-monitoring system requires:

- Representative and correctly labelled images.
- Appropriate object detection architecture.
- Consistent data preprocessing.
- Independent evaluation using suitable metrics.
- Testing under different visual conditions.

These findings provide the basis for developing and evaluating SmartShelf AI.

## 📚 4. Academic References

1. YOLO Research Paper — background on object detection
https://arxiv.org/abs/1506.02640

2. Ultralytics YOLO Documentation — model training, prediction, and evaluation
https://docs.ultralytics.com/

3. YOLO Performance Metrics — precision, recall, and mAP
https://docs.ultralytics.com/guides/yolo-performance-metrics/

4. Retail Shelf Monitoring Research — research related to your project
https://scholar.google.com/scholar?q=retail+shelf+monitoring+computer+vision

5. Roboflow Universe — explore computer vision datasets
https://universe.roboflow.com/.

## 🗂️ 5. Dataset Description

The model's performance depends on the dataset used to train and evaluate it.

| Dataset detail    | Project information                          |
| ----------------- | -------------------------------------------- |
| Dataset name      | [Enter actual dataset name]                  |
| Data source       | [Enter source or download link]              |
| Data type         | Images and object annotations, if applicable |
| Number of images  | [Enter actual image count]                   |
| Object classes    | [List actual classes]                        |
| Annotation format | [Enter actual format]                        |

### 5.1 Data Preparation

The data preparation process should document the steps actually performed:

1. **Data collection:** Obtain the images from the selected dataset.
2. **Data inspection:** Check image quality, file formats, missing files, and duplicate images.
3. **Annotation verification:** Confirm that object labels and bounding boxes are valid.
4. **Preprocessing:** Apply the image resizing, normalisation, or augmentation used by the model pipeline.
5. **Dataset splitting:** Separate the data into training, validation, and testing sets.
6. **Data verification:** Confirm that the images, annotations, and class identifiers match correctly.

### 5.2 Training and Testing Split

| Subset     | Percentage | Purpose                                    |
| ---------- | ---------: | ------------------------------------------ |
| Training   | [Actual %] | Used to learn model parameters             |
| Validation | [Actual %] | Used to monitor training and tune settings |
| Testing    | [Actual %] | Used for final evaluation                  |

The percentages and image counts must match the actual dataset split used in the experiment.

## 🧠 6. Model Architecture

**Model used:** [Enter the exact model name and version from the code]

If the implementation uses Ultralytics YOLO, document the precise model variant, such as the relevant YOLOv8 model size, rather than describing all YOLO variants as interchangeable.

### Model Workflow

1. An image is provided to the application.
2. The image is prepared for model inference.
3. The trained model predicts object classes and bounding boxes.
4. Predictions are filtered according to the configured confidence threshold.
5. The resulting detections are displayed in the application.
6. Any stock-level interpretation is calculated using the logic implemented in the project.

### Why Object Detection?

Object detection is useful when a system needs to determine both **what an object is** and **where it appears in an image**.

The suitability of the chosen architecture should ultimately be assessed using the project's measured performance and application requirements.

## ⚙️ 7. Model Training Configuration

Record the actual parameters from the training script or saved training configuration.

| Parameter                      | Actual value                  |
| ------------------------------ | ----------------------------- |
| Model architecture and weights | [Enter value]                 |
| Number of epochs               | [Enter value]                 |
| Image size                     | [Enter value]                 |
| Batch size                     | [Enter value]                 |
| Optimiser                      | [Enter value]                 |
| Learning rate                  | [Enter value]                 |
| Confidence threshold           | [Enter value]                 |
| Data augmentation              | [Enter techniques used]       |
| Hardware                       | [Enter CPU/GPU, if known]     |
| Training framework             | [Enter framework and version] |

### Training Techniques

Describe the techniques that were actually used:

- **Transfer learning:** State whether pretrained weights were used.
- **Data augmentation:** Document any flips, scaling, colour adjustments, or other transformations.
- **Validation:** Explain how validation data was used during training.
- **Hyperparameter tuning:** Describe any parameters tested and how the final configuration was selected.

Do not list a technique as implemented unless it is supported by the training code or experiment records.

## 📊 8. Model Evaluation and Results

The trained model should be evaluated on an independent test set to measure how well it detects objects in images it has not seen during training.

### 8.1 Evaluation Metrics

| Metric         | Meaning                                                                              |
| -------------- | ------------------------------------------------------------------------------------ |
| Precision      | Proportion of predicted positive detections that are correct                         |
| Recall         | Proportion of ground-truth objects that the model successfully detects               |
| mAP\@0.50      | Mean average precision at an IoU threshold of 0.50                                   |
| mAP\@0.50:0.95 | Mean average precision averaged over IoU thresholds from 0.50 to 0.95                |
| Inference time | Time taken to produce predictions for an input, measured under documented conditions |

**Accuracy note:** For object detection, precision, recall, and mAP are generally more informative than a single classification accuracy percentage. Report classification accuracy only if the task and evaluation procedure make that metric appropriate.

### 8.2 Experimental Results

| Metric                 |                    Measured result |
| ---------------------- | ---------------------------------: |
| Precision              |                    [Actual result] |
| Recall                 |                    [Actual result] |
| mAP\@0.50              |                    [Actual result] |
| mAP\@0.50:0.95         |                    [Actual result] |
| Test images evaluated  |                     [Actual count] |
| Average inference time | [Actual measurement, if available] |

Results should be copied from the actual evaluation output. Specify whether values are expressed as percentages or decimals.

### 8.3 Results Analysis

After evaluation, discuss:

- Which object classes achieved the strongest results.
- Which classes produced missed detections or false positives.
- Whether the model performed consistently across different images.
- How image quality, object size, lighting, or occlusion affected performance.
- Whether the model was sufficiently fast for the intended application.

The final analysis should be based on measured results and observed predictions, not assumed performance.

## 🖥️ 9. Application and Demo Screenshots

Screenshots should show the actual running application and its outputs.

### 9.1 Main Dashboard



*Figure 1: Main application dashboard.*

### 9.2 Image Upload and Detection



*Figure 2: Example input image and model predictions.*

### 9.3 Model Results



*Figure 3: Example results or performance visualisation.*

**Screenshot instructions:** Create a `screenshots` folder in your repository and save your real screenshots using the filenames shown above. If a screen does not exist in your application, remove that subsection rather than using a placeholder image.

## 🚀 10. Installation and Execution

### Prerequisites

- Python version compatible with the project's dependencies.
- Git.
- Required Python libraries.
- Model weights and dataset files, if needed for local inference or training.

### Step 1: Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_REPOSITORY_FOLDER>
```

### Step 2: Install dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Run the application

Replace `app.py` with the actual entry-point filename if required.

```bash
streamlit run app.py
```

### Step 4: Open the application

Open the local URL displayed by Streamlit in your browser.

## 📁 11. Project Structure

Update this example to match the actual repository.

```text
SmartShelf-AI/
├── app.py
├── requirements.txt
├── README.md
├── screenshots/
│   ├── dashboard.png
│   ├── detection.png
│   └── results.png
├── models/
│   └── [trained model weights]
└── dataset/
    └── [dataset files, if included]
```

Do not upload large datasets or model files unless their licences and repository limits permit it.

## ⚠️ 12. Limitations

Potential limitations to investigate include:

- Performance on product types absent from the training dataset.
- Changes in lighting, camera angle, or image quality.
- Occluded or overlapping products.
- Differences between the training images and real-world shelf images.
- The difference between detecting a product and determining actual inventory quantities.

Image-based detections do not automatically guarantee an accurate count of physical stock. The result depends on the model, image coverage, and counting logic implemented.

## 🔮 13. Future Improvements

Potential future improvements include:

- Expanding the dataset with more varied shelf images.
- Improving annotation quality and class balance.
- Evaluating alternative model architectures.
- Optimising inference speed.
- Adding confidence-aware alerts and clearer performance reports.
- Testing the system on independently collected real-world images.

