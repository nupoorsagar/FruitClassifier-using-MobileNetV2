# FruitClassifier-using-MobileNetV2
A lightweight fruit classification model optimized for real-world applications such as assisting visually impaired individuals in identifying fruits, enhancing automated checkouts in grocery stores and supporting inventory systems in agriculture and retail

Presentation:
https://docs.google.com/presentation/d/1XuoXTyeKZCTCrUAULf7IOnxzxo6jIGe2a498KVxm-vY/edit?usp=drive_link
<img width="927" height="516" alt="image" src="https://github.com/user-attachments/assets/03398336-1ca6-41ac-9d26-8ce172678cd2" />


Fruit Classification Model Enhancement: Boosting Accuracy (68.69% to 84.44%)
This presentation details our advanced fruit classification model, built on MobileNetV2. We analyzed and implemented a prior paper, then developed a robust methodology to overcome its flaws, significantly improving validation accuracy.

Key Flaws Identified in Previous Work:

1. Misclassification: Poor performance on real-world images with varied lighting/backgrounds.

2. Overfitting: Excessive training epochs (30) led to memorization.

3. Suboptimal Architecture: Lacked Global Average Pooling (GAP); small Kernel (3x3) & Stride (1) hindered efficiency.

Our Approach & Improvements:

1. Preprocessing:
* Input Image Size: Increased from 32x32 to 96x96 for better feature preservation.
* Background Removal: Applied threshold-based masking to isolate fruits.
* CLAHE Enhancement: Improved color/texture visibility in varying light conditions.
* Normalization: Images scaled to [0, 1] for better convergence.

2. Optimized Training Setup:
* Dataset: 2,876 images (9 classes) from augmented Kaggle data, validated with a custom real-world image test set.
* Batch Size: 32.
* Epochs: Reduced to 20 to mitigate overfitting.
* Optimizer: Adam (lr = 1e-4), more effective than 0.001.
* Loss Function: Categorical Cross Entropy.

Results & Impact:

1. Lower training time due to optimized epochs.
2. Better feature representation from higher resolution and CLAHE.
3. Improved generalization through balanced augmentation and architectural refinements.

Resultant lightweight model suitable for mobile deployment, offering real-world applications. This includes assisting visually impaired individuals in fruit identification, enhancing automated checkouts in grocery stores, and supporting inventory systems in agriculture and retail by providing precise and timely fruit classification.
