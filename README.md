# Atari-Breakdown-Deep-Q-Network

## Description

This code is my implementation of the following paper in which a Deep-Q Network is trained using visual inputs to play the BreakOut Atari Game- 
https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf

### Dependencies

* Python 3.8.8
* gym  0.7.4
* tensorflow 2.6.0
* keras 2.6.0
* keras-rl2 1.0.5
* Pillow 8.4.0

### Code

* The preprocessing notebook details the image preprocessing pipeline required before the training process. The game display before and after pre-precoessing looks like-

![original](https://user-images.githubusercontent.com/57484266/137694789-4b00dd3f-cd29-48f5-9c92-36fbfcacc0c4.PNG) ![preprocessed image](https://user-images.githubusercontent.com/57484266/137689641-0fa54deb-c52f-4b61-b76d-2b21ec9fe897.png)


* The DQN notebook has the code for training your own dqn model. It also has code snippets to evaluate model performance on my pre-trained weights which have been trained
for 1.2 million episodes. You can train your own model from scratch, start training from where I left or just see what my model has achieved.

### Results

1) Performance after 100000 epsiodes-
* Episode 1: reward: 0.000, steps: 123 
* Episode 2: reward: 0.000, steps: 123  
* Episode 3: reward: 0.000, steps: 123 
* Episode 4: reward: 0.000, steps: 123 
* Episode 5: reward: 0.000, steps: 123 


https://user-images.githubusercontent.com/57484266/137689723-ac3fe7bd-e4a6-40f1-a747-6310fb6cc4bd.mp4


2) Performance after 1.1 million epsiodes-
* Episode 1: reward: 28.000, steps: 976 
* Episode 2: reward: 28.000, steps: 976 \n
* Episode 3: reward: 28.000, steps: 976
* Episode 4: reward: 28.000, steps: 976
* Episode 5: reward: 28.000, steps: 976


https://user-images.githubusercontent.com/57484266/137689754-bf823c28-029d-4dd1-924b-b50c04e2a64d.mp4


3) Performance after 1.1 million epsiodes-
* Episode 1: reward: 40.000, steps: 1513
* Episode 2: reward: 40.000, steps: 1513
* Episode 3: reward: 40.000, steps: 1513
* Episode 4: reward: 40.000, steps: 1513
* Episode 5: reward: 40.000, steps: 1513


https://user-images.githubusercontent.com/57484266/137689791-31778e74-d751-42cf-a565-794f40f8d564.mp4


You can observe that the model is able to understand how to play the game and achieve human like scores after 1.2 million episodes of training. 
Note that the "reward" mentioned in the results and the "score" shown during the game are 2 different things. Reward is something which is defined inside the environment
for the learning process, whereas score comes into the picture when we are actually playing the game. Both increase after training.
