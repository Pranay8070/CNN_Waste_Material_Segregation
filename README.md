# CNN_Waste_Material_Segregation



---

## 📌 Project Summary

This project addresses the challenge of classifying waste images into **7 categories**: *Cardboard, Food Waste, Glass, Metal, Paper, Plastic,* and *Other*. A custom **Convolutional Neural Network (CNN)** was implemented using the `Keras Sequential` API, trained on resized RGB images of size **128×128×3**.

The dataset exhibits significant **class imbalance**, with *Plastic* being the most frequent and *Cardboard* the least. To mitigate this, **real-time data augmentation** techniques were applied using `ImageDataGenerator`, including rotation, translation, shear, zoom, and flipping transformations. Labels were extracted from folder names and one-hot encoded for compatibility with multi-class classification.

### 🔍 Key Highlights:

* **Model**: 3-layer CNN with `BatchNormalization`, `Dropout`, `ReLU`, and `Softmax` for output.
* **Training Accuracy**: \~95%
* **Validation Accuracy**: Improved from \~64% to \~69% after applying data augmentation.
* **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix.
* **Imbalance Handling**: Augmentation + future support for class weighting or resampling.

The network was trained with early stopping and learning rate reduction to prevent overfitting. Despite strong training performance, validation accuracy highlighted the difficulty in classifying similar-looking classes like *Plastic* and *Food Waste*. Data augmentation helped close the gap between train and validation metrics, improving generalization.

This project demonstrates the importance of preprocessing and model regularization when dealing with real-world, imbalanced image datasets. Future improvements could include the use of **transfer learning** (e.g., ResNet, MobileNet), **focal loss**, or **automated augmentation search (AutoAugment)**.

---

