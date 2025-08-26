# Celebrity Face Recognition using Azure AI

This project involved building and comparing two different facial recognition models on the Microsoft Azure cloud platform to classify images of celebrities. The goal was to gain hands-on experience with Azure's Machine Learning pipelines and Custom Vision service.

##  Project Structure
Azure-Face-Recognition/
├── README.md # This file (Project overview & documentation)
├── Assigment_2.pdf # Full project report
└── assets/ # Folder for screenshots of results
└── confusion_matrix.png

##  Objective

To develop and compare the performance of two image classification approaches:
1.  A custom-built pipeline using **Azure Machine Learning** and the **DenseNet** model.
2.  A no-code solution using **Azure Custom Vision**.

##  Dataset

The dataset consisted of **300 high-resolution images** (300 dpi), evenly distributed across three classes:
- `Angelina Jolie` (100 images)
- `Brad Pitt` (100 images)
- `Denzel Washington` (100 images)

**Data Preparation:** Images were resized and cropped to ensure consistent dimensions and to focus on the facial region. They were organized into separate folders for each class, a requirement for supervised learning.

## ⚙ Methodology

### 1. Azure Machine Learning Pipeline
- **Components Used:** Convert to Image Directory, Split Image Directory, Init/Apply Image Transformation, DenseNet model, Train PyTorch Model, Score Image Model, Evaluate Model.
- **Training/Validation Split:** 90% Training, 10% Validation.
- **Epochs:** 2
- **Key Steps:** 
  - Initialized image transformations (used default values).
  - Applied transformations to both training and validation sets.
  - Trained a DenseNet model on the prepared data.
  - Evaluated the model's performance on the validation set.

### 2. Azure Custom Vision
- **Training Type:** Quick Training
- **Process:** Uploaded images and tagged them with the respective celebrity names. The service handled the rest of the pipeline automatically.

##  Results

### Azure ML Pipeline (DenseNet)
- **Overall Accuracy:** **0.9**
- **Micro/Macro Precision:** ~0.9
- **Confusion Matrix:**
  - Angelina Jolie: 90%
  - Brad Pitt: 90%
  - Denzel Washington: 100%

### Azure Custom Vision
- **Overall Performance:** 
  - **Precision:** 98.3%
  - **Recall:** 98.3%
  - **AP (Average Precision):** 99.9%
- **Performance Per Tag:**
  | Celebrity           | Precision | Recall | AP    |
  |---------------------|-----------|--------|-------|
  | Denzel Washington   | 100.0%    | 100.0% | 100.0%|
  | Angelina Jolie      | 100.0%    | 100.0% | 100.0%|
  | Brad Pitt           | 96.0%     | 96.0%  | 99.8% |

##  Conclusion & Learnings

This project provided valuable insights into two distinct approaches to AI on Azure:

*   **Azure Machine Learning Pipeline** offered greater flexibility and transparency into the training process (e.g., configuring the train/validation split, seeing a confusion matrix). It was instrumental in understanding how validation data size impacts model performance.
*   **Azure Custom Vision** was significantly faster and more practical to implement, providing excellent results with minimal setup, making it ideal for rapid prototyping.

The project demonstrated the end-to-end process of a computer vision task, from data preparation and model training to evaluation and comparison of different solutions.

##  Skills Demonstrated

`Azure Machine Learning` `Azure Custom Vision` `Computer Vision` `Image Classification` `DenseNet` `Data Preprocessing` `Model Evaluation` `MLOps` `Cloud Computing`
