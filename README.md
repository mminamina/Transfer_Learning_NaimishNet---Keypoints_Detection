# Transfer Learning Project: Facial Keypoints_Detection
Project 1: Facial Keypoints Detection with **NaimishNet**
### Project Experience
This is the version with **NaimishNet** for my first computer vision project which allows me to apply deep learning computer vision architectures (using **Pytorch**) to build a facial keypoint detection system for
- tracking
- pose recognition
- filters
- emotion recognition
### Image Augmentation
Introduce generalization(randomness) to detect and learn structures
### Transform Steps
Only the following transformation techniques were chosen to avoid unnecessary impacts on keypoints
- **Rescale** to 250 for width and height
- **RandomCrop** to 224
- **Normalize & Convert ToTensor**

### Architecture & Performance
NaimishNet is applied here as TransferLearning. (Compared to the model without using TransferLearning: https://github.com/mminamina/Udacity_ComputerVision_PeerReviewed_Project---Facial_Keypoints_Detection)

BatchSize, Epochs, Loss & Optimization Functions(using **GPU**)
- **BatchSize** : 32 for train dataset and 20 for test dataset
- **Epochs**   : 6 (can train longer for better performance)
- **Loss**     : SmoothL1Loss (significant loss reduction since earlier epochs)
- **Optimizer** : Adam 

NaimishNet with four **Conv2D** layers, **ReLU** Activation, **MaxPooling**+**BatchNorm** in every layer, three **fully-connected** layers, and **Dropout**  to prevent overfitting.

### Worklist
For project instructions, please refer to https://github.com/udacity/P1_Facial_Keypoints

### Files in Order
- models.py;
- Notebook 2. Define the Network Architecture.ipynb
- Notebook 3. Facial Keypoint Detection, Complete Pipeline.ipynb

### Results
- NaimishNet seems to generate more accurate keypoints compared to my original work without TransferLearning
- Please refer to https://github.com/mminamina/Udacity_ComputerVision_PeerReviewed_Project---Facial_Keypoints_Detection


