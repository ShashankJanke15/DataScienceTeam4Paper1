# DataScienceTeam4Paper1
# CartPole-v1 DQN (SO2-Tuned) - Reproducibility Guide
This repository contains the code to reproduce the SO2-Tuned DQN results on the CartPole-v1 environment, following the methodology inspired by the SO2 paper.

# Training in Google Colab
This project was successfully trained and evaluated on Google Colab to ensure reproducibility without needing a local GPU.

Steps to Run in Colab:
# 1.Upload/Clone Code
Upload the project files manually into Colab, or clone from GitHub.
# 2 Install Required Packages
!pip install --upgrade pip
!pip install git+https://github.com/opendilab/DI-engine.git@main#egg=DI-engine
!pip install gymnasium pyvirtualdisplay imageio matplotlib numpy
# 3 Environment Setup
CartPole-v1 environment (gymnasium) is lightweight, no special hardware setup is needed.
For video recording:
!apt-get install -y xvfb
!pip install pyvirtualdisplay

# 4 Training
You can run the training scripts directly from Colab cells:
Train Vanilla DQN
!python train_dqn.py

Train SO2-Tuned DQN
!python train_so2_dqn.py
# 5 Evaluation & Video Generation

After training, run evaluation scripts to record and save gameplay videos.

You can download videos from Colab to your local machine easily.

# 6 Downloading Results
Trained model checkpoints

Evaluation videos

Reward plots
from google.colab import files
files.download('path_to_file')
