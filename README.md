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
