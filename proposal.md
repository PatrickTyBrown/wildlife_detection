# Project Proposal

 
### **Client:** <br>

The client is a Wildlife Conservation Organization. <br>

***

### **Question/Need:**<br>


The organization works to preserve lands home to biodiversity and sensitive wildlife populations. A large component of this process is understanding and tracking wildlife populations and behaviors. 
<br>

The goal of this project is to develop a system for the organization to identify wildlife present. 
<br>

***

### **Data Description:**<br>

We will be using the [Open Images Dataset](https://storage.googleapis.com/openimages/web/index.html) by Google. The dataset is quite large so we will be limiting it to relevant labels for our wildlife detection. We will then using images as our feature set. We will use labels and bounding boxes as our targets.<br>
***

### **Solution Path:**<br>
We see our solution to this problem as two stage:

1. Create a general purpose model as a proof of concept. 
     - We will use a [YOLO](https://arxiv.org/abs/1506.02640) like model for predicting our classes and boxes.  
     - We will not be concerned with model speed or size here.
2. Create a smaller specialize model.*
    - Utilze First model as a teacher. Perform knowledge distilation for training the smaller model. See [Keras implementation](https://keras.io/examples/vision/knowledge_distillation/) as a resource. 

- **Feature Engineering**
    - Images will need to be resized to a smaller resolution.
    - Images may be augmented to help generalization to images in the wild. 
- Model
  - YOLO* 
  - Faster rCNN
  - rFCN

<sub>*See Constraints</sub><br>
<sub>**Leading option</sub>
<br>

***

### **Criteria for Success:**<br>

- Our model is able to detect the presence of wildlife in naturalistic images. 
- Our model is lightweight enough to run on a small device.*

<sub>*See Constraints</sub>
<br>

***

### **Assumptions, Risks and Constraints:**<br>

The organization will need to gather data from remote regions where access to the internet may be unavailable. The will need to gather data from large areas requiring many monitoring points. This scale will make it infeasible for the organization to deploy stations with network capabilities. Without the ability to uploud images regularly storage will become an issue. The smaller model we can develop the easier it will be to deploy in specialize devices with limited compute. Rather than storing images, we will only need to store records of the wildlife scene. 
<br>

Our data augmentation strategy will generalize to real life incoming documentation.
<br>
***

### **Tools:**<br>
1. Keras
2. Numpy
3. OpenCV
4. Gradio
5. Albumentations
6. Google Colab

<br>

***

### **Communication:**<br>
A slide presentation will be made explaining the model building process and showcasing the model utility.

A demo web app will be presented allowing for live demonstration of the tool. 

<br>

***

### **MVP Goal:**<br>

An MVP for this project will consist of a model generated to detect the presence of a small number of animals.
