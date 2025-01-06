# AI/ML Football Analysis System with YOLO, OpenCV, and Python

This project demonstrates how to create a football analysis system using machine learning, computer vision, and deep learning techniques. The system utilizes YOLO (You Only Look Once) for object detection, OpenCV for image processing, and Python for scripting.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Setup](#setup)
- [Usage](#usage)
- [Datasets](#datasets)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Introduction
In this project, we build an AI/ML football analysis system that can detect players, referees, and footballs in videos. The system tracks these objects across frames, assigns players to teams based on t-shirt colors, measures camera movement, and calculates player speed and distance covered.

## Features
- **Object Detection**: Uses YOLOv8 to detect objects in images and videos.
- **Custom Training**: Fine-tunes and trains YOLO on a custom dataset.
- **Player Color Assignment**: Uses KMeans clustering to segment players based on t-shirt colors.
- **Camera Movement Estimation**: Uses optical flow to measure camera movement between frames.
- **Perspective Transformation**: Represents the scene's depth and perspective to measure player movement in meters.
- **Speed and Distance Calculation**: Calculates player speed and distance covered.

## Setup
Follow these steps to set up the project:

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/abdullahtarek/football-analysis.git
   cd football-analysis
   ```

2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

3. **Download Datasets**:
   - Kaggle Dataset: [Kaggle Competition Dataset](https://www.kaggle.com/competitions/dataset)
   - Roboflow Football Dataset: [Roboflow Dataset](https://universe.roboflow.com/roboflow/football-dataset)

4. **Set Up Folders**:
   Organize the datasets and model weights in the appropriate folders as demonstrated in the video.

## Usage
1. **Run Object Detection**:
   ```sh
   python detect.py --source path_to_video --weights path_to_weights
   ```

2. **Train Custom Model**:
   ```sh
   python train.py --data path_to_data --cfg path_to_cfg --weights path_to_weights
   ```

3. **Player Color Assignment**:
   ```sh
   python color_assignment.py --source path_to_video
   ```

4. **Camera Movement Estimation**:
   ```sh
   python camera_movement.py --source path_to_video
   ```

5. **Speed and Distance Calculation**:
   ```sh
   python speed_distance.py --source path_to_video
   ```

## Datasets
- **Kaggle Dataset**: Contains videos and annotations for training the object detection model.
- **Roboflow Football Dataset**: Provides additional data for training and validation.

## Results
The system can accurately detect and track players, referees, and footballs in videos. It assigns players to teams based on t-shirt colors, measures camera movement, and calculates player speed and distance covered.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
