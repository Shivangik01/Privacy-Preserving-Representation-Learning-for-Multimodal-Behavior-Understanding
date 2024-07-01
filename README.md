# Privacy-Preserving Representation Learning for Multimodal Behavior Understanding

## Introduction
Behavior understanding, particularly through the analysis of biometric features such as voice patterns and facial expressions, holds significant promise for applications like emotion recognition and speech recognition. However, the utilization of such personal information raises substantial privacy concerns, particularly regarding the potential for unauthorized identification or surveillance. 

In this research paper, we propose an approach focused on learning representations of behavior that are informative for downstream tasks while safeguarding individuals’ privacy. Our goal is to develop techniques that extract meaningful insights from behavior data without compromising individuals’ anonymity. Through this project, we aim to explore various methods to preserve representation learning while ensuring privacy. With increasing data collection and privacy concerns, we identified this as an area that requires active attention and research.

## Project Information
- **Course:** CSCI 535: Multimodal Probabilistic Learning of Human Communication
- **Contributors:** 
  - Aabha Ranade
  - Ravi Vivek Agrawal
  - Shivangi Kochrekar
  - Vaidehi Vatsaraj

## Methodology
### Video Component
1. **Image Preprocessing:** Resizing, adding noise.
2. **Training the Autoencoder:** 
   - Learning rate: [0.01, 0.001]
   - Optimizers: [Adam, SGD]
   - Loss: Mean Squared Error (MSE)
   - Batch size: [32, 64]
   - Epochs: [50, 100, 150]
   - Latent space size: 300
3. **Model Accuracy:** 84.65%
4. **Video to Frames:** Convert video to frames and preprocess.
5. **Reconstructed Frames:** Get reconstructed image of each frame using the saved model.
6. **Combine Frames:** Combine reconstructed frames to make video.
7. **Emotion Recognition:** Test video for emotion recognition using a pre-trained model.
8. **Speaker Identification:** Test using pre-trained VGG16 model.

### Audio Component
1. **Extracting Audio:** Extracting audio features.
2. **Extracting MFCCs:** Mel Frequency Cepstral Coefficients (MFCCs).
3. **Creating Noise:** Setting sensitivity and epsilon (Sensitivity: 0.5 and Epsilon: 0.8).
4. **Clustering MFCCs:** Using K-means algorithm.
5. **Reconstructing Audio:** Using centroids of the MFCCs.
6. **Emotion Recognition:** Training a Random Forest model.
7. **Speaker Identification:** 
   - Trained CNN model.
   - Pre-trained model application.

## Results
- **Emotion Recognition Task:**
  - Accuracy of 64.3% with late fusion.
  - Audio module: 78% accuracy.
  - Video module: 39.7% accuracy.
- **Video Privacy Model:** 95% accuracy in hiding user identity.
- **Audio Privacy Model:** Significant accuracy in hiding user identity.
- **Challenges:**
  - Video privacy while maintaining emotional features is complex.
  - Audio privacy is relatively less intricate.
  - 3D mesh generation is computationally heavy.

## Takeaways
- Privacy is a critical concern with increasing AI model usage.
- Further research is required in this domain to balance utility and privacy.
