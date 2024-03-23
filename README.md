**This repository contains code and instructions for training a YOLOv7 model for helmet detection and deploying it using DeepStream.**


**Features:**

-Trains a YOLOv7 model on a helmet detection dataset.

-Exports the trained model to ONNX format.

-Converts the ONNX model to a TensorRT engine for optimized inference.

-Uses DeepStream for real-time object detection with the TensorRT engine.


**Installation:**

Clone this repository.

https://github.com/WongKinYiu/yolov7


**Requirements:**
 1. See the requirements.txt in the clone directory. Make sure all the requirements are satisfied before start training the model.
 2. To get the engine file and deployment on the deepstream app, make sure you have a Jetson device with the following requirements.
    
  • Hardware Platform (Jetson / GPU): Jetson Orin Nano or above
  
  • DeepStream Version: deepstream-6.4
  
  • JetPack Version : Version: 6.0-b52
  
  • TensorRT Version: Version: 8.6.2

**How to proceed:**
1. Train the YOLOv7 model: Train the YOLov7 using Transfer Learning on your dataset and get the best.pt model. (You can use the above added file) 
2. Export to ONNX: use the export_yoloV7.py to get the ONNX file.
3. Convert to TensorRT Engine: Use the following command to get the engine file on the Jetson device. (Use it as a reference )
   
   `/usr/src/tensorrt/bin/trtexec --onnx=best.onnx --saveEngine=best_yolo_model.engine`


4. Deploy with DeepStream: Use this as a reference: https://github.com/marcoslucianops/DeepStream-Yolo


**Results:**
![test_batch0_labels](https://github.com/AnilSarode/Yolov7-helmetDetection/assets/42278309/05de06a3-73ae-407f-8ab1-3308ed1d00c8)

![test_batch1_labels](https://github.com/AnilSarode/Yolov7-helmetDetection/assets/42278309/d43cbf2f-3cef-43ad-81ae-77cae98ddd12)

**Disclaimer:**
 
 1. This is a sample project and may require modifications for production use.
 2. The code is intended for educational purposes only.


