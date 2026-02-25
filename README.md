# Traffic Sign Recognition using Convolutional Neural Networks (CNN)

![Deep Learning](https://img.shields.io/badge/Model-CNN-blue)
![Accuracy](https://img.shields.io/badge/Accuracy-98.7%25-green)
![Dataset](https://img.shields.io/badge/Dataset-GTSRB-orange)

## 📌 Project Overview
[cite_start]This project focuses on the development of a machine learning program for **Traffic Sign Recognition** using Convolutional Neural Networks (CNN)[cite: 3]. [cite_start]The system is designed to provide a foundation for automated road transportation by identifying traffic signs under various environmental conditions[cite: 7, 11].

## 📊 Data Analysis
[cite_start]The model is trained on the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset[cite: 14].

* [cite_start]**Dataset Size**: Over 50,000 images in total[cite: 4, 14].
* [cite_start]**Class Distribution**: 43 distinct classes of traffic signs[cite: 4, 15].
* [cite_start]**Training/Testing Split**: Approximately 39,000 images for training and 12,000 for testing[cite: 15].
* [cite_start]**Handling Imbalance**: The original dataset was imbalanced, leading to potential misclassification of under-sampled signs like "keep right" or "go straight"[cite: 17, 18]. 
* [cite_start]**Oversampling Strategy**: Underrepresented classes were oversampled to match the class with the highest number of images, creating a balanced dataset for training[cite: 19, 20].

![Class Distribution](C:\Users\Aarya-2\Documents\ADOG\AARYA_PERSONAL\PROJECTS\TEMU_NEURIPS\Main_GTSRB_program\IMPORTANT_PROJECTS\Project-Traffic_Signals\Paper-ready-project\output.png)

## 🏗️ Model Architecture
[cite_start]The approach uses a deep CNN architecture to capture complex image features through multiple layers[cite: 5].



### Layer Specifications:
1.  [cite_start]**Input Layer**: $30 \times 30 \times 3$ RGB images[cite: 31, 32].
2.  [cite_start]**Convolutional Layers**: Four layers using 32, 64, 128, and 256 filters respectively ($3 \times 3$ size) with **ReLU** activation[cite: 34, 38, 43, 46].
3.  [cite_start]**Pooling Layers**: Two Max-Pooling layers ($2 \times 2$) to reduce computational power while retaining important features[cite: 41, 48].
4.  [cite_start]**Global Average Pooling**: Used to convert 2D features into a 1D vector to reduce parameters and prevent overfitting[cite: 50, 52].
5.  [cite_start]**Fully Connected (Dense) Layers**: Three dense layers (512, 256, and 128 neurons) to build complex representations[cite: 56, 60, 64].
6.  [cite_start]**Regularization**: Integrated **Batch Normalization** and **Dropout** (ranging from 30% to 50%) to ensure stable training and prevent memorization[cite: 42, 57, 58, 62].
7.  [cite_start]**Output Layer**: 43 neurons with **Softmax** activation to predict class probabilities[cite: 68, 69].

![Model Summary](C:\Users\Aarya-2\Documents\ADOG\AARYA_PERSONAL\PROJECTS\TEMU_NEURIPS\Main_GTSRB_program\IMPORTANT_PROJECTS\Project-Traffic_Signals\Paper-ready-project\CNN_model.png)

## 🚀 Training & Performance
[cite_start]The model was optimized using the **Adam optimizer** and **Categorical Crossentropy** loss[cite: 74, 76].

* [cite_start]**Early Stopping**: Implemented to halt training when validation loss stopped improving[cite: 77].
* [cite_start]**Learning Rate Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate ($0.001$ base) when the model reached a performance plateau[cite: 75, 78].
* **Final Results**:
    * [cite_start]**Test Accuracy**: 98.749% [cite: 95]
    * [cite_start]**Precision Score**: 0.980 [cite: 97]
    * [cite_start]**Recall Score**: 0.979 [cite: 98]

## 🔍 Challenges & Limitations
[cite_start]Despite high performance, approximately 1.3% of signs remain undetected due to extreme conditions[cite: 108]:
* [cite_start]**Distortions**: Signs covered by shadows or tree branches[cite: 109].
* [cite_start]**Environmental Factors**: Sun gleam or weather conditions making signs unrecognizable to the naked eye[cite: 109, 115].

## 📜 References
* [cite_start][GTSRB Dataset (Kaggle)](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign) [cite: 117]
* [cite_start]Educative: Image and Pattern Recognition [cite: 117]
