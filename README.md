# Aksara Jawa Classification with CNN (VGG-16)

## Overview
This project focuses on the classification of Javanese script characters using a Convolutional Neural Network (CNN) with VGG-16 architecture. The dataset used for training and testing comes from Roboflow and Kaggle. The goal is to classify 20 distinct Javanese characters, including Ba, Ca, Da, Dha, Ga, Ha, Ja, Ka, La, Ma, Na, Nga, Nya, Pa, Ra, Sa, Ta, Tha, Wa, and Ya.

## Training Details
- **Date:** Saturday, August 10, 2024
- **Location:** Lab Data Monetize
- **Model Version:** v4.4.8

## Dataset
- **Sources:** Roboflow and Kaggle
- **Number of Classes:** 20 Javanese script characters
  - Ba, Ca, Da, Dha, Ga, Ha, Ja, Ka, La, Ma, Na, Nga, Nya, Pa, Ra, Sa, Ta, Tha, Wa, Ya

## Libraries Used
The following libraries were utilized in this project:
1. TensorFlow
2. Keras
3. OpenCV
4. NumPy
5. Pandas
6. Matplotlib
7. Seaborn
8. Scikit-learn

## Preprocessing Techniques
The preprocessing steps applied to the images include:
1. **Inter-Area Interpolation**: Used for resizing images.
2. **Grayscale Conversion**: Converts images to grayscale.
3. **Laplacian of Gaussian (LoG)**: Edge detection technique.
4. **Thresholding**: Image binarization.
5. **Reshape and Normalization**: Ensures uniform input shape and normalizes pixel values.

## Model Architecture
The CNN model is based on the **VGG-16** architecture with the following specifications:
- **Optimizer**: SGD
- **Batch Normalization**: No parameters
- **Dropout Rate**: 0.2
- **Learning Rate**: 0.0001
- **Weight Decay**: 0.0001
- **Momentum**: 0.9
- **Batch Size**: 64
- **Number of Layers**: 5
- **Epochs**: 350

## Results
The trained model achieved the following performance metrics:

1. **Accuracy**:
   - Training Accuracy: **0.99**
   - Testing Accuracy: **0.94**
   
2. **Loss**:
   - Testing loss reduced significantly from **0.92** at epoch 50 to **0.28** around epoch 200.
   
3. **Precision**:
   - Highest precision of **1.00** for the characters: **ba, ja, ka, nya, ra, and tha**.
   - Lowest precision for the character: **ta**.

4. **Recall**:
   - Highest recall of **1.00** for the characters: **nga and ra**.
   - Lowest recall of **0.84** for the character: **ya**.

5. **F1-Score**:
   - Highest F1-score of **1.00** for the character: **ra**.
   - Lowest F1-score of **0.88** for the character: **ta**.

## Conclusion
Overall, the model demonstrates strong performance with an accuracy of 0.94 on the test set, but there are still areas for improvement in recognizing certain Javanese characters. The unique complexity of Javanese script presents challenges in achieving perfect generalization, but the current results are promising and provide a solid foundation for further development.

## Future Improvements
- Enhance the recognition of characters with lower recall and precision values, particularly **ta** and **ya**.
- Explore additional preprocessing techniques to better handle the intricate shapes of Javanese characters.
- Experiment with different CNN architectures and hyperparameters to further improve the model's robustness.
