# Automated Checkout
## Problem Statement : 
To build a an automated checkout system that generates the bill with video object detection.
## About Dataset :
The image dataset collected comprises of 50-50 images each of the products in various categories. These products include: -
1) Bread
2) Butter
3) Eggs
4) Coconut
5) Milk

![Screenshot 2022-08-06 113055](https://user-images.githubusercontent.com/81613474/183236451-17c08422-05ad-488a-a9d0-6a24c7ac717f.png)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Screenshot 2022-08-06 113113](https://user-images.githubusercontent.com/81613474/183236453-bcdd82dc-97e0-402b-b514-5ad3af8a53c8.png)

Image data collected through web scraping

## Toolkit :
### Robo Flow
Robo flow is a Computer Vision developer framework for better data collection to 
pre-processing, and model training techniques. Robo flow also offers the option to 
create a dataset using a split that the user defines.
#### 1) Pre processing
In pre-processing, there was inbuilt feature in Roboflow for giving annotations. We 
put labels on each of the photos. Along with this, Roboflow increased our dataset by 
rotating every image with different angles. So, now we have approx. 2000 images as 
compared to earlier where we have 720 images
#### 2) Data Production
In this process, Roboflow divided our dataset into three folders, that is, Training
Testing and validation. In each of these folders, there were 2 subfolders- images and 
labels. Data.yml files extracted all the labels which we gave and then allotted 
respective labels on respective items. 
After processing the dataset from Robo flow we got 1 API key and then used that to 
import data in yolo for further detection.

### YOLOv5
YOLO is one of the most famous object detection algorithms due to its speed and accuracy.
I used YOLO V5 which is model trained on COCO dataset and which uses a 
transfer learning technique. I tuned this model on our dataset to get better 
accuracy for object detection.

### User Interface - Tkinter
Tkinter is the standard GUI library for Python. Python when combined with Tkinter 
provides a fast and easy way to create GUI applications. Tkinter provides a powerful 
object-oriented interface to the Tk GUI toolkit

![Screenshot 2022-08-06 115632](https://user-images.githubusercontent.com/81613474/183237411-9bc87941-732e-4970-8c1d-8506d26ef787.png)

## Methods :
1. Used python code for web scrapping
2. Used Robo Flow for image annotation, pre-processing and augmentation.
3. Used YOLOv5 as a model.
   You can view the model and model summary from `model.ipynb` file
4. Trained YOLOv5 with custom dataset. Transfer learning
5. Used Tkinter for GUI. 
6. Video get detected after we upload a video file.

## Installation :
### Steps to run the application
To run this code in your local system you have to download this repository using-

git clone https://github.com/nakulvarma2000/Automated_Checkout.git

Now open the downloaded directory and install the required python packages using-

pip install -r requirements.txt

Now open `AutomatedCheckoutApp.ipynb` and run all the cell. The last cell runs the GUI

## Training and Evaluation
I have used google colab for training this YOLOv5 model.

CPU : Xeon Processors @2.3Ghz

GPU : Tesla T4, 15110MiB

## Further Modification’s:
1. Improve the result accuracy by increasing the size of dataset.
2. Run the model on high end hardware to reduce prediction latency.

