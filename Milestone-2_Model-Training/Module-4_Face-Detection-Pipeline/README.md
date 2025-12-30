## Module 4: Face Detection and Prediction Pipeline

### Objective
To detect faces from input images and perform facial skin condition prediction using the trained CNN model.

### Face Detection Strategy
A **hybrid face detection approach** was implemented to improve robustness:

1. **Primary Method**
   - OpenCV Haar Cascade was used for face detection due to its simplicity and fast performance.

2. **Fallback Method**
   - MediaPipe Face Detection was used as a **fallback mechanism** when Haar Cascade failed to detect a face.
   - This ensured better detection accuracy across varying lighting conditions, poses, and image qualities.

### Prediction Pipeline
- Detected face regions were cropped and resized to 224 × 224.
- Preprocessed faces were passed to the trained EfficientNetB0 model.
- Predictions were displayed as class labels with confidence percentages.
- Bounding boxes were drawn around detected faces.

### Outputs
- Face bounding boxes on input images
- Predicted skin condition with probability scores

### Deliverables
- Face detection and prediction script/notebook
- Sample output images with annotations
- Haar Cascade and MediaPipe integration

### Outcome
The fallback strategy improved face detection reliability and ensured consistent prediction results across diverse images.

