# YOLOv8 Object Detection and Siamese Network for Face Recognition

This repository contains code that demonstrates how to train YOLOv8 for object detection tasks and use a Siamese network for face recognition tasks. The YOLOv8 model is trained on a custom face detection dataset, and the Siamese network utilizes the FaceNet model for face recognition.

![YOLOv8](https://github.com/ozzmanmuhammad/Face-detection-YOLOv8-and-Recognition-with-SIAMESE-Network/assets/93766242/561f0329-9493-4852-a1ed-4fd1063c7f3d)

---
The YOLOv8 part will run easily on colab but for the Siamese network, you will need to download the 
pretrained model for the FaceNet model and run the code on the local machine for python 2.7 and tensorflow 2.3.0.
### Installation for YOLOv8


1. Clone the repository:

   ```
   git clone <repository-url>
   ```

   It is recommended to create a new environment and install the required packages.

2. Install the Ultralytics YOLOv8 package:

   ```
   pip install ultralytics==8.0.20
   ```

   Alternatively, you can use the Git clone method for development. Refer to the Ultralytics YOLOv8 documentation for more information.

### Usage for YOLOv8

1. Object Detection with YOLOv8:

   - Run YOLOv8 inference on a pretrained COCO model using the command line interface (CLI):

     ```
     yolo task=detect mode=predict model=yolov8n.pt conf=0.25 source=<image-path> save=True
     ```

   - Alternatively, use the Python SDK:

     ```python
     from ultralytics import YOLO

     model = YOLO('yolov8n.pt')
     results = model.predict(source='<image-path>', conf=0.25)
     ```

2. Custom Training with YOLOv8:

   - Prepare a custom dataset in the required format.
   - Train the YOLOv8 model using the CLI:

     ```
     yolo task=detect mode=train model=yolov8s.pt data=<data-path> epochs=25 imgsz=800 plots=True
     ```

   - Validate the custom model:

     ```
     yolo task=detect mode=val model=<trained-model-path> data=<data-path>
     ```

   - Run inference with the custom model:

     ```
     yolo task=detect mode=predict model=<trained-model-path> conf=0.25 source=<image-path> save=True
     ```

## Face Recognition with Siamese Network:
On the local machine for python 2.7 and tensorflow 2.3.0 run the remaining code in the notebook.
The pretrained model for the is attached in the repository.

### Installation for Siamese Network

1. Set up the environment for:

   - Python 3.7
   - TensorFlow 2.3.0
   - Keras 2.4.3

2. Install the required packages:

   ```
   pip install -r requirements.txt
   ```

## License

This code is licensed under the [MIT License](LICENSE).

---
