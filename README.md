# Rice Leaf Disease Detection using CNN
This deep learning project aims to detect and classify rice leaf diseases into three categories using Convolutional Neural Networks (CNNs) and Transfer Learning.

# Problem Statement
Build an image classification system to detect:

Leaf Smut

Brown Spot

Bacterial Leaf Blight

The project includes data preprocessing, model training (Custom CNN and pre-trained networks), and performance evaluation — to identify the best approach for production deployment.

# Dataset Summary
Collected ~120 labeled rice leaf images across 3 disease categories.

Dataset had class imbalance and missing samples (addressed in preprocessing).

Images resized and normalized for model input.

# Workflow Overview
## Image Preprocessing
Resized, normalized, and converted images to NumPy arrays

Handled class imbalance by duplicating underrepresented classes

Performed stratified train-test split

## Data Augmentation
Applied real-world image transformations to improve generalization:

Rotation (up to 30°)

Zoom (±20%)

Horizontal & vertical flips

Brightness adjustment

Rescaling (1./255)

## Models Implemented
### Custom CNN Model
3 Convolutional layers + MaxPooling

Flatten + Dense layers with ReLU + Dropout

Accuracy: ~83%

Performed best due to its simplicity & augmentation support

### MobileNetV2 (Transfer Learning)
Pre-trained on ImageNet, fine-tuned last few layers

Accuracy: ~33%

Lightweight but failed due to small dataset

### Heavy architecture with limited fine-tuning

Did not generalize well

### EfficientNetB0
Modern architecture, fast inference

Similar performance limitations as other pre-trained models

## Evaluation Highlights
Model	Accuracy	Notes
Custom CNN	83%	Best overall
MobileNetV2	33%	Poor generalization
ResNet50	~40%	Slightly better, still weak
EfficientNetB0	~45%	No significant improvement

## Key Insights
Custom CNN worked best due to small dataset size and effective augmentation.

Transfer Learning models struggled due to data sparsity.

Data Augmentation significantly reduced overfitting in Custom CNN.
