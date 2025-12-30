## Module 3: Model Training using EfficientNetB0

### Objective
To train a CNN model for facial skin condition classification using transfer learning.

### Model Details
- Base Model: EfficientNetB0 (pretrained on ImageNet)
- Loss Function: Categorical Cross-Entropy
- Optimizer: Adam
- Metrics: Accuracy

### Training Process
- Fine-tuned top layers of EfficientNet
- Trained using augmented dataset
- Monitored training and validation performance

### Deliverables
- Trained model (.h5)
- Accuracy and loss plots
- Training notebook

### Result
Achieved stable validation accuracy close to expected benchmark.

