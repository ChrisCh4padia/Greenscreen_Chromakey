# Greenscreen_Chromakey
Captures Stream of Webcam and replaces with a custom picture

## What you'll need
* Python 3.9.X and above

## How to Setup

1. Install python Packages: `opencv-python, cvzone, mediapipe`
2. Clone Repository
3. Run in command line via cmd: 
   `python app.py`

Note: The App can be closed by pressing "c" or Interrupting the process with Ctrl-C 

## Features

1. Dynamic Background image selection:

Included in the repo is an "Image" folder.
After running the app, it scans the folder for pictures and puts them in an array. 
You can then cycle through pictures using the "+" and "-" keys.
Please note that the pictures need to have the same or a greater resolution as the webcam.

2. Screenshot functionality:

You can take a screenshot of the current window by pressing the key "s". The screenshot will be saved in the local screenshot directory.

## GUI

Graphical userinterface written in Golang for command line shy people

![image](https://user-images.githubusercontent.com/87771733/221035422-2f88add7-e66a-434e-95c4-4e5babf16634.png)

This really just calls the app.py program with some parameters

## Command line parameters

-ns or --noslide: Removes the slider from the app

-ok or --onlykeyed: Shows only the final picture with the adjusted background, no webcam feed or slider.

-h or --help: Shows the help information

-t or --threshold: Threshold value to adjust the segmentation. Default value is 0.8.

-b or --background: Diesplay the background picture next to the video output. Combineable with "-ok"

-nfps or --nofps: Turn off the fps reader that reads the current framerate of the camera

## Command line Examples

1. Display the keyed out window next to the background with thresholdslider:
   
   `python3 -b -ok`

2. Display only the keyed out window with a threshold of 0.5 and no thresholdslider:
   
   `python3 -ok -ns -t 0.5`

3. Display the background image. the original camera stream and the keyed out window with thresholdslider. Removes fps reader :
   
   `python3 -b -nfps`

## TODO

1. Implement Dynamic Threshold Adjustment
2. Add logging functions
