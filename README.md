# Groceries Detection

## Overview
This project focuses on detecting store products belonging to **43 different classes** using deep learning. Examples of detected products:

<p align="center">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Granny-Smith.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Pink-Lady.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Lemon.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Banana.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Vine-Tomato.jpg" width="150">
</p>
<p align="center">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Yellow-Onion.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Green-Bell-Pepper.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Arla-Standard-Milk.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Oatly-Natural-Oatghurt.jpg" width="150">
  <img src="https://github.com/marcusklasson/GroceryStoreDataset/raw/master/sample_images/natural/Alpro-Fresh-Soy-Milk.jpg" width="150">
</p>

---

## Deep Learning Approaches

We experiment with two deep learning architectures:

### 1️⃣ Custom CNN  
- **Objective**: Achieve >60% accuracy.  
- **Results**: Our network obtained **~65% accuracy** on the validation set.  
- **Robustness Check**: We trained the model **five times** to ensure stable results.  

#### Training Results  
![Custom CNN Accuracy](https://github.com/user-attachments/assets/325fd5bf-c1ec-4fba-8e66-23923597ad70)

- We also conducted an **ablation study** to analyze the contribution of different network components.

---

### 2️⃣ ResNet Fine-Tuning  
- **Objective**: Achieve **80-90% accuracy**.  
- **Experiments**:
  1. **Feature Extractor Frozen** (ResNet backbone not trained)  
     - Achieved **~82% accuracy** on the validation set.  
     ![ResNet Frozen](https://github.com/user-attachments/assets/94463c8d-9922-4b89-b598-1d48da44cdcb)

  2. **Last Layer Trained** (Fine-tuning the last layer of ResNet)  
     - Achieved **~90% accuracy** on the validation set.  
     ![ResNet Fine-Tuned](https://github.com/user-attachments/assets/83467931-eaf6-41ad-8338-2102e30ebec7)
