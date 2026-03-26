
## Author
Repalle Eswar Venkat

Student ID: 24165064
# One-Class SVM for Image Anomaly Detection
##Do Machine Learning Models Understand Images or Just Pixel Patterns?
A Study Using One-Class Support Vector Machines and Image Distortions

## Overview
This project investigates whether machine learning models truly understand images or rely on pixel-level patterns. A One-Class Support Vector Machine (SVM) is trained on the Fashion-MNIST dataset and evaluated on distorted images to study robustness.

## Objectives
- Train One-Class SVM using normal image data
- Apply distortions (blur, noise, edge-only) to test robustness
- Analyze how distortions affect model performance
- Understand whether the model captures structure or pixel statistics

## Dataset
- Fashion-MNIST dataset
- 28x28 grayscale images of clothing items
- Images flattened into 784-dimensional vectors
- Training samples: 12,000
- Testing samples: 3,000

## Methodology
- Preprocess images using normalization (z-score)
- Train One-Class SVM with RBF kernel
- Hyperparameters:
  - Kernel: RBF
  - Gamma: 0.01
  - Nu: 0.1
- Evaluate model on:
  - Original images
  - Blurred images
  - Noisy images
  - Edge-detected images

## Key Results
- Model shows moderate performance on original images (~48%)
- Blur improves performance (~73%) due to smoothing effect
- Noise and edge distortions cause severe performance drop (~100% anomaly detection)
- Model is highly sensitive to pixel-level changes

## Insights
- One-Class SVM relies on pixel distributions rather than image structure
- Flattening images removes spatial relationships
- Model lacks robustness to high-frequency distortions
- Indicates limitation in traditional ML compared to deep learning

## Installation
Install required libraries using:
pip install numpy matplotlib scikit-learn opencv-python pandas

## How to Run
1. Open Jupyter Notebook
2. Load the file: eswar_venkat_one_svm.ipynb
3. Run all cells sequentially
4. View generated plots and results

## Outputs
- Dataset visualization
- Distorted image examples
- Detection accuracy comparison
- Performance drop graphs
- Decision boundary distribution plots

## Repository Structure
- eswar_venkat_one_svm.ipynb : Main notebook
- README.md : Project documentation
- requirements.txt : Dependencies
- figures/ : Output plots (optional)

## References
- Schölkopf, B., et al. (2001). Estimating the support of a high-dimensional distribution
- Geirhos, R., et al. (2019). ImageNet-trained CNNs are biased towards texture
- Xiao, H., et al. (2017). Fashion-MNIST dataset

## Ethical Considerations
- Anomaly detection systems can produce false positives
- Bias in training data may affect fairness
- Care must be taken in real-world deployment (e.g., healthcare, security)

## License
This project is licensed under the MIT License.


