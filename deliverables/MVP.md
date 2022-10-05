# Wildlife Detection
#### Minimum Viable Product

 
### **Goal:** <br>

The goal of this project is to develop a system for identifying if wildlife is present in an area. 
<br>

***

### **Getting Started:**<br>

We leveraged the configuration and training set ups [published](https://github.com/ultralytics/yolov5) by the makers of the YOLO model. We then utilized a [dataset published on Roboflow](https://universe.roboflow.com/hcl/all_animals21) for object detection with various animals. We were then able to train the preconfigured model with our new data. 
***

### **The task:**<br>
The goal of the model is 2 fold:

1. The model performs regresses bounding boxes around the recognized entities in the image.
2. The model classifies those entities.
  
***
![Training Performance](https://github.com/PatrickTyBrown/wildlife_detection/blob/main/assets/training_perf.png?raw=true)
![Training Loss](https://github.com/PatrickTyBrown/wildlife_detection/blob/main/assets/training_loss.png?raw=true)