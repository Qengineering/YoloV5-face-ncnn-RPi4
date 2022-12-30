# YoloV5 face Raspberry Pi 4
![output image]( https://qengineering.eu/github/Face_selfie_1920_out.webp )
_target size 1920._
## YoloV5 face recognition with the ncnn framework. <br/>
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
Paper: https://arxiv.org/pdf/2105.12931.pdf<br><br>
Special made for a bare Raspberry Pi 4, see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html)

------------

## Benchmark.
| Model  | framework | model |size |  mAP | Jetson Nano<br/>2015 MHz | RPi 4 64-OS<br/>1950 MHz |
| ------------- | :-----: | :-----:  | :-----:  | :-----:  | :-------------:  | :-------------: |
| Ultra-Light-Fast| ncnn | slim-320 | 320x240 | 67.1  |    - FPS | 26 FPS |
| Ultra-Light-Fast| ncnn | RFB-320 | 320x240 | 69.8  |    - FPS | 23 FPS |
| Ultra-Light-Fast| MNN | slim-320 | 320x240 | 67.1  | 70 FPS | 65 FPS |
| Ultra-Light-Fast| MNN | RFB-320 | 320x240 | 69.8  | 60 FPS | 56 FPS |
| Ultra-Light-Fast| OpenCV | slim-320 | 320x240 | 67.1  | 48 FPS | 40 FPS |
| Ultra-Light-Fast| OpenCV | RFB-320 | 320x240 | 69.8  | 43 FPS | 35 FPS |
| Ultra-Light-Fast + Landmarks| ncnn | slim-320 | 320x240 | 67.1  | 50 FPS | 24 FPS |
| LFFD| ncnn | 5 stage | 320x240 | 88.6 | 16.4 FPS | 4.85 FPS |
| LFFD| ncnn | 8 stage | 320x240 | 88.6 | 11.7 FPS | 3.45 FPS |
| LFFD| MNN | 5 stage | 320x240 | 88.6 | 2.6 FPS | 2.17 FPS |
| LFFD| MNN | 8 stage | 320x240 | 88.6 | 1.8 FPS | 1.49 FPS |
| CenterFace| ncnn | - | 320x240 | 93 | 16.5 FPS | 6.8 FPS |
| YoloV5 face | ncnn | - | 320x320 | 93.6 |  - FPS | **17.2 FPS** |
| YoloV5 face | ncnn | - | 480x480 | 93.6 |  - FPS | **7.2 FPS** |
| YoloV5 face | ncnn | - | 640x640 | 93.6 |  - FPS | **4.0 FPS** |
| YoloV5 face | ncnn | - | 1280x1280 | 93.6 |  - FPS | **1.0 FPS** |
| YoloV5 face | ncnn | - | 1920x1920 | 93.6 |  - FPS | **0.5 FPS** |

------------

## Dependencies.
To run the application, you have to:
- A raspberry Pi 4 with a 32 or 64-bit operating system. It can be the Raspberry 64-bit OS, or Ubuntu 18.04 / 20.04. [Install 64-bit OS](https://qengineering.eu/install-raspberry-64-os.html) <br/>
- The Tencent ncnn framework installed. [Install ncnn](https://qengineering.eu/install-ncnn-on-raspberry-pi-4.html) <br/>
- OpenCV 64 bit installed. [Install OpenCV 4.5](https://qengineering.eu/install-opencv-4.5-on-raspberry-64-os.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)

------------

## Installing the app.
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/YoloV5-face-ncnn-RPi4/archive/refs/heads/main.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip, LICENSE and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm LICENSE <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
9.jpg <br/>
11.jpg <br/>
26.jpg <br/>
selfie.jpg <br/>
YoloV5-face.cpb <br/>
main.cpp <br/>
yolov5-blazeface.bin <br/>
yolov5-blazeface.param <br/>

------------

## Running the app.
To run the application load the project file YoloV5-face.cbp in Code::Blocks. More info or<br/> 
The accuracity depends on the target size which can be set in `main.cpp` at line 30 `face_detector.detect(m, objects, 640);`.
if you want to connect a camera to the app, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/><br/>
![output image]( https://qengineering.eu/github/Face_selfie_1280_out.webp) 
_target size 1280._ <br><br>
![output image]( https://qengineering.eu/github/Face_selfie_640_out.webp) 
_target size 640._ <br><br>
![output image]( https://qengineering.eu/github/Face_26_out.jpg) 
_target size 640._ 

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 

