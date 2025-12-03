Brain Tumor Prediction with CNN & VGG16
Overview:
    This project explores how deep learning can be applied to medical imaging, specifically brain MRI scans. Using both a custom Convolutional Neural Network (CNN) and transfer learning with VGG16, the goal is to classify MRI images into different tumor types and “no tumor” cases. The idea is to show how a simple CNN compares against a proven pre-trained model like VGG16, and how transfer learning can boost accuracy when working with limited medical datasets.

Dataset:
    The dataset contains MRI images grouped into four categories:
        Glioma
        Meningioma
        Pituitary
        No Tumor
All images are resized to 200×200 pixels and normalized before training. (Add your dataset source here, e.g., Kaggle or a medical imaging repository.)

Approach:
1. Preprocessing
    Resize and normalize images
    Apply augmentation (rotation, flipping, zoom) to improve generalization
    Split into training and validation sets

2. Custom CNN
    Several convolution + max pooling layers
    Flatten and dense layers for classification
    Softmax output for multi-class prediction

3. Transfer Learning with VGG16
    Load VGG16 pre-trained on ImageNet (without the top layer)
    Freeze base layers to retain general features
    Add custom dense layers for tumor classification
    Fine-tune deeper layers for improved accuracy

Results:
    The custom CNN provides a good baseline but struggles with complex patterns.
    VGG16 transfer learning achieves higher accuracy and generalization.
