<h1 align="center">Face Mask Detection</h1>

  <h4>Face Mask Detection System built with OpenCV, Keras/TensorFlow using Deep Learning and Computer Vision concepts in order to detect face masks in static images as well as in real-time video streams.</h4>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Python](https://img.shields.io/badge/python-v3.6+-blue.svg)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555)](https://www.linkedin.com/in/naveen-vinayak-s/)


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Live Demo](https://github.com/NaveenVinayakS/Mask_Detection/blob/main/Readme_images/Fask_mask_detection.gif)


## :innocent: Motivation
Amid the ongoing COVID-19 pandemic, there are no efficient face mask detection applications which are now in high demand for transportation means, densely populated areas, residential districts, large-scale manufacturers and other enterprises to ensure safety. The absence of large datasets of __‘with_mask’__ images has made this task cumbersome and challenging. 


<p align="center"><img src="https://github.com/NaveenVinayakS/Mask_Detection/blob/main/Readme_images/Screen%20Shot%202020-05-14%20at%208.49.06%20PM.png" width="700" height="400"></p>


## :warning: TechStack/framework used

- [OpenCV](https://opencv.org/)
- [Caffe-based face detector](https://caffe.berkeleyvision.org/)
- [Keras](https://keras.io/)
- [TensorFlow](https://www.tensorflow.org/)
- [MobileNetV2](https://arxiv.org/abs/1801.04381)

## :star: Features
Our face mask detector doesn't use any morphed masked images dataset and the model is accurate. Owing to the use of MobileNetV2 architecture, it is computationally efficient, thus making it easier to deploy the model to embedded systems (Raspberry Pi, Google Coral, etc.).

This system can therefore be used in real-time applications which require face-mask detection for safety purposes due to the outbreak of Covid-19. This project can be integrated with embedded systems for application in airports, railway stations, offices, schools, and public places to ensure that public safety guidelines are followed.

## :file_folder: Dataset
The dataset used can be downloaded here - [Click to Download](https://github.com/NaveenVinayakS/Mask_Detection/tree/main/dataset)

This dataset consists of __4095 images__ belonging to two classes:
*	__with_mask: 2165 images__
*	__without_mask: 1930 images__

The images used were real images of faces wearing masks. The images were collected from the following sources:

* __Bing Search API__ ([See Python script](https://github.com/NaveenVinayakS/Mask_Detection/blob/main/search.py))
* __Kaggle datasets__ 
* __RMFD dataset__ ([See here](https://github.com/X-zhangyang/Real-World-Masked-Face-Dataset))

## :key: Prerequisites

All the dependencies and required libraries are included in the file <code>requirements.txt</code> [See here](https://github.com/NaveenVinayakS/Mask_Detection/blob/main/requirements.txt)

## 🚀&nbsp; Installation
1. Clone the repo
```
$ git clone https://github.com/NaveenVinayakS/Mask_Detection.git
```

2. Change your directory to the cloned repo 
```
$ cd Face-Mask-Detection
```

3. Create a Python virtual environment named 'test' and activate it
```
$ virtualenv test
```
```
$ source test/bin/activate
```

4. Now, run the following command in your Terminal/Command Prompt to install the libraries required
```
$ pip install -r requirements.txt
```

## :bulb: Working

1. Open terminal. Go into the cloned project directory and type the following command:
```
$ python train_mask_detector.py --dataset dataset
```

2. To detect face masks in an image type the following command: 
```
$ python detect_mask_image.py --image images/pic1.jpeg
```

3. To detect face masks in real-time video streams type the following command:
```
$ python detect_mask_video.py 
```
## :key: Results

#### Our model gave 98% accuracy for Face Mask Detection after training via <code>tensorflow-gpu==2.5.0</code>

####          
![](https://github.com/NaveenVinayakS/Mask_Detection/blob/main/Readme_images/Screenshot%202020-06-01%20at%209.48.27%20PM.png)

#### We got the following accuracy/loss training curve plot
![](https://github.com/NaveenVinayakS/Mask_Detection/blob/main/plot.png)

## Streamlit app

Face Mask Detector webapp using Tensorflow & Streamlit

command
```
$ streamlit run app.py 
```
## Images

<p align="center">
  <img src="Readme_images/1.PNG">
</p>
<p align="center">Upload Images</p>

<p align="center">
  <img src="Readme_images/2.PNG">
</p>
<p align="center">Results</p>

## :clap: And it's done!
Feel free to mail me for any doubts/query 
:email: naveenvinayak.2195@gmail.com

---

## Internet of Things Device Setup

### Expected Hardware
* [Raspberry Pi 4 4GB with a case](https://www.canakit.com/raspberry-pi-4-4gb.html)
* [5MP OV5647 PiCamera from Arducam](https://www.arducam.com/docs/cameras-for-raspberry-pi/native-raspberry-pi-cameras/5mp-ov5647-cameras/)

### Getting Started
* Setup the Raspberry Pi case and Operating System by following the Getting Started section on page 3 at `documentation/CanaKit-Raspberry-Pi-Quick-Start-Guide-4.0.pdf` or https://www.canakit.com/Media/CanaKit-Raspberry-Pi-Quick-Start-Guide-4.0.pdf
  * With NOOBS, use the recommended operating system
* Setup the PiCamera
  * Assemble the PiCamera case from Arducam using `documentation/Arducam-Case-Setup.pdf` or https://www.arducam.com/docs/cameras-for-raspberry-pi/native-raspberry-pi-cameras/5mp-ov5647-cameras/
  * [Attach your PiCamera module to the Raspberry Pi and enable the camera](https://projects.raspberrypi.org/en/projects/getting-started-with-picamera/2)

### Raspberry Pi App Installation & Execution

> Run these commands after cloning the project

| Commands                                                                                                                     | Time to completion |
|------------------------------------------------------------------------------------------------------------------------------|--------------------|
| sudo apt install -y libatlas-base-dev liblapacke-dev gfortran                                                                | 1min               |
| sudo apt install -y libhdf5-dev libhdf5-103                                                                                  | 1min               |
| pip3 install -r requirements.txt                                                                                             | 1-3 mins           |
| wget "https://raw.githubusercontent.com/PINTO0309/Tensorflow-bin/master/tensorflow-2.4.0-cp37-none-linux_armv7l_download.sh" | less than 10 secs  |
| ./tensorflow-2.4.0-cp37-none-linux_armv7l_download.sh                                                                        | less than 10 secs  |
| pip3 install tensorflow-2.4.0-cp37-none-linux_armv7l.whl                                                                     | 1-3 mins           |

---
