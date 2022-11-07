# TensorFlow_Lite_Classification_RPi_zero
![output image]( https://qengineering.eu/images/Schoolbus2.png )
## TensorFlow Lite classification running on a bare Raspberry Pi Zero
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
A 'fast' C++ implementation of TensorFlow Lite classification on a bare Raspberry Pi zero.<br>
Be noted that we use the zero version here, not the new Raspberry Pi zero 2.<br/>
Inference time: 11 sec<br/>
Special made for a Jetson Nano see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html) <br/>

------------

Papers: https://arxiv.org/pdf/1712.05877.pdf <br/>
Training set: COCO with 1000 objects<br/>
Size: 224x224 <br/>


------------

## Dependencies.<br/>
To run the application, you have to:
- TensorFlow Lite framework installed. [Install TensorFlow Lite](https://qengineering.eu/install-tensorflow-2-lite-on-raspberry-pi-4.html#Zero) <br/>
- OpenCV installed. [Install OpenCV 4.5](https://qengineering.eu/install-opencv-4.5-on-raspberry-pi-4.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)

------------

## Installing the app.
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/TensorFlow_Lite_Classification_RPi_zero/archive/refs/heads/master.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
tabby.jpeg <br/>
schoolbus.jpg <br/>
grace_hopper.bmp <br/>
Labels.txt <br/>
TensorFlow_Lite_Mobile.cpb <br/>
TensorFlow_Lite_Class.cpp<br/>
 <br/>
Next, choose your model from TensorFlow: https://www.tensorflow.org/lite/guide/hosted_models <br/> 
Download a quantized model, extract the .tflite from the tarball and place it in your *MyDir*. <br/> <br/>
Now your *MyDir* folder may contain: mobilenet_v1_1.0_224_quant.tflite. <br/>
Or: inception_v4_299_quant.tflite. Or both of course. <br/> <br/>
Enter the .tflite file of your choice on line 54 in TensorFlow_Lite_Class.cpp <br/>
The image to be tested is given a line 84, also in TensorFlow_Lite_Class.cpp <br/> <br/>

------------

## Running the app.
Run TestTensorFlow_Lite.cpb with Code::Blocks. More info or<br/> 
if you want to connect a camera to the app, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/><br/>

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 
