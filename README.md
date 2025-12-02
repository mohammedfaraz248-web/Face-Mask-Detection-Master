Face Mask Detection Using TensorFlow in Python

This project is a deep-learning–based face mask detector built using TensorFlow, Keras, and OpenCV.
It can classify whether a person is wearing a mask or not wearing a mask in both images and real-time video.


---

🚀 Features

Trainable deep learning model (binary classification)

Uses MobileNetV2 transfer learning

Real-time detection using webcam

High accuracy on mask vs no-mask classes

Includes pre-trained mask_detector.model



---

📂 Project Structure

├── face detector/            # Face detection model (deploy.prototxt & .caffemodel)
├── with_mask/                # Training images: people with masks
├── without_mask/             # Training images: people without masks
├── detect_mask_video.py      # Real-time mask detection script
├── train_mask_detector.py    # Model training script
├── mask_detector.model       # Saved trained model
├── requirements.txt          # List of required libraries
├── plot.png                  # Training accuracy/loss graph
└── README.md


---

🛠 Installation

⿡ Clone the repository

git clone <your_repo_link>
cd <your_repo_folder>

⿢ Install all required libraries

pip install -r requirements.txt

⿣ Make sure TensorFlow is installed

If using CPU:

pip install tensorflow

If using GPU:

pip install tensorflow-gpu


---

🎯 Training the Model

If you want to retrain the model:

python train_mask_detector.py

After training, a new mask_detector.model file will be created, along with a training graph (plot.png).


---

🎥 Running Real-Time Detection

To run face mask detection using webcam:

python detect_mask_video.py

Press Q to stop the video window.


---

💡 How It Works

1. Face detection is done using OpenCV’s Deep Learning face detector (Caffe model).


2. The detected face is passed to the MobileNetV2-based classifier.


3. The model predicts:

Mask

No Mask



4. Results are displayed on the video frame.




---

📦 Requirements

Key dependencies (all included in requirements.txt):

TensorFlow

Keras

OpenCV

NumPy

Imutils

Matplotlib



---

📝 Notes

The dataset used here contains two classes: with_mask and without_mask.

You can add more images to improve accuracy.

You can replace the Caffe face detector with other models if needed.
