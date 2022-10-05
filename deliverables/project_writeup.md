## Wildlife Monitoring

****
<br/>

#### By: Patrick Brown

## **Case**
Conservation organizations monitor wildlife populations. This can be difficult in remote and expansive areas. Deploying trail cameras can be costly and require reviewing large amounts of footage/images. 

Using deep learning we hope to create a model that can be deployed cheaper and save review time.

## **Design**
We treated this as an object detection problem. We needed to identify if/what wildlife is present and where. To do this, we leveraged the configuration and training set ups [published](https://github.com/ultralytics/yolov5) by the makers of the YOLO model. Yolo (You only look once) is a SOTO model that can run extremely quickly.

## **Data**
We then utilized a [dataset published on Roboflow](https://universe.roboflow.com/hcl/all_animals21). This dataset includes 20 different animal labels. It contains 17,277 images which were divided into a train (12072) validation (1711) and test set(3494).

## **Tools**
- pyTorch
- Numpy
- Google Colab

## **Conclusions**
Our final model achieved a mean Average Precision of 0.771. The model performed well on the data with a relatively small size. The performance was affected by class imbalance in our data. To move forward, we will want to explore expanding our dataset and further shrinking our model for effecient deployment.

## **Communication**
End results were presented via a slide presentation and published to GitHub.