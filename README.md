# Problem Statement


### Business Understanding

You are required to develop a cool feature in a smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:
1) Thumbs up:  Increase the volume
2) Thumbs down: Decrease the volume
3) Left swipe: 'Jump' backwards 10 seconds
4) Right swipe: 'Jump' forward 10 seconds  
5) Stop: Pause the movie


### Data Understanding

The training data consists of a few hundred videos categorised into one of the five classes. Each video typically 2-3 seconds long is divided into a sequence of 30 frames/images. These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

The dataset contains a 'train' and a 'val' folder with two CSV files for the two folders. These folders are in turn divided into subfolders where each subfolder represents a video of a particular gesture. Each subfolder, i.e. a video, contains 30 frames/images. Note that all images in a particular video subfolder have the same dimensions but different videos may have different dimensions. Specifically, videos have two types of dimensions - either 360x360 or 120x160 depending on the webcam used to record the videos.

Each row of the CSV file represents one video and contains three main pieces of information - the name of the subfolder containing the 30 images of the video, the name of the gesture and the video's numeric label between 0-4.


### Business Goal

Train a model on the 'train' data which performs well on the 'val' data. We have withheld the test dataset for internal evaluation purposes.
