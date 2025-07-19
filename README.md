# Using Python programming to Play Grand Theft Auto 5

Explorations of Using Python to play Grand Theft Auto 5, mainly for the purposes of creating self-driving cars and other vehicles.

We read frames directly from the desktop, rather than working with the game's code itself. This means it works with more games than just GTA V, and it will basically learn (well, attempt to learn...) whatever you put in front of it based on the frames as input and key presses as output.

Pull requests are welcomed.

Currently, to use the latest version of this AI, you will need to run first "create_training_data.py," then balance this data with "balance_Data.py."

When creating training data, this works when you have the game in windowed mode, 800x600 resolution, at the top left of your screen. You need this for both training and testing. Eventually we can go off the window's name, but, for now, the current code wants the window in the corner.

Do this for as many files/training samples as you wish. I suggest 100K+ after balancing, but the more the merrier.

Next, Train the model with train_model.py.

Finally, use the model in game with test_model.py. 

...you'll probably want to poke into the tutorials here: https://pythonprogramming.net/game-frames-open-cv-python-plays-gta-v/. If you need tutorials on deep learning, or tensorflow, or tflearn, see here: https://pythonprogramming.net/tensorflow-introduction-machine-learning-tutorial/

# 🚗 GTA 5 Autonomous AI Driver using Computer Vision and Deep Learning

This project showcases an AI-powered **Autonomous Driving Agent** for GTA V built using **OpenCV**, **Deep Learning (CNNs)**, and **TensorFlow 2.0**. The system captures the driver’s in-game view, processes the visual input to detect road lanes and obstacles, and sends simulated keystrokes to control the car — all in real time.

> 🎥 Demo Videos:
> - [GTA5 AI Driver](./GTA5%20AI%20DRIVER.mp4)
> - [Computer Vision in Action](./GTA%205%20COMPUTER%20VISION.mp4)

---

## 🧠 Key Features

- **Real-Time Lane Detection**: Uses OpenCV to identify lanes and process road boundaries.
- **CNN-Based Decision System**: Trained a Convolutional Neural Network to classify road scenarios and predict driving actions.
- **Self-Driving Logic**: AI agent decides when to accelerate, steer, or slow down based on live visual feed.
- **Crash Avoidance**: Detects obstacles to ensure safe navigation.

---

## 🛠️ Technologies Used

- **Language:** Python
- **Libraries:** OpenCV, NumPy, TensorFlow 2.0, Keras
- **Tools:** PyAutoGUI / DirectInput for key simulation, Windows Screen Capture
- **Game:** GTA V (PC Version)

---

## 🧪 Workflow

1. **Data Collection**  
   - Captured screen frames during manual gameplay.
   - Labeled the data with the associated key presses (`W`, `A`, `D`, etc.).

2. **Preprocessing**  
   - Converted frames to grayscale or RGB.
   - Cropped to focus on the road and resized images to reduce training time.

3. **Model Training**  
   - Trained a CNN on the processed dataset with action labels.
   - Evaluated over multiple epochs to avoid overfitting.

4. **Inference and Control**  
   - AI predicts the correct driving action for each frame in real time.
   - Simulated keystrokes sent to GTA V using key control libraries.

---

### 🚀 Getting Started
---


## Prerequisites:

GTA V (PC version)

Python 3.7+

TensorFlow, OpenCV, NumPy, Pickle, etc.

---

# Install dependencies
pip install -r requirements.txt

# Train the model
python train.py

# Run the AI driver
python gta_ai_driver.py

---

## 🏁 Results
The AI agent successfully tested and drives across highways and roads while avoiding crashes in GTA-5 Simulation.

Seamless integration between vision, decision-making, and control.

Performance improves with more data and fine-tuning CNN architecture.

---

## 🤖 Future Improvements
Implement reinforcement learning for long-term strategy.

Add traffic sign and pedestrian detection.

Port to real-world simulators like CARLA.

---

## 🙋‍♂️ Author
Raghav Garg
📧 raghavgarg92004@gmail.com
🌐 LinkedIn
🐙 GitHub

---

## ⭐ If you like this project, don't forget to star the repo!

---

