# TensorFlow_Lite_Classification_RPi_zero
TensorFlow Lite classification running on bare Raspberry Pi Zero

A fast C++ implementation of TensorFlow Lite classification on a bare Raspberry Pi 4.
Inference time: 11 sec

https://arxiv.org/pdf/1712.05877.pdf <br/>
Training set: COCO with 1000 objects<br/>
Size: 224x224 <br/>
Special made for a bare Raspberry Pi see: https://qengineering.eu/install-tensorflow-2-lite-on-raspberry-pi-4.html <br/>
<br/>
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
Run TestTensorFlow_Lite.cpb with Code::Blocks. Remember, you also need a working OpenCV 4 on your Raspberry. <br/>
Preferably use our installation: https://qengineering.eu/install-opencv-4.3-on-raspberry-pi-4.html <br/>

![output image]( https://qengineering.eu/images/Schoolbus2.png )
