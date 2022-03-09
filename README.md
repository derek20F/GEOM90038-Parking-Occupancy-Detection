# GEOM90038 Advanced Imaging 2021 SM1
## Parking occupancy detection from CCTV images

### Summary
*	Trained Faster RCNN model to detect vehicles in parking area
*	Clustered the detected vehicles using spatio-temporal analysis to find the coordinates of individual parking slots
*	Implemented ResNet as a classifier to predict the occupancy within each parking slot.


### D

In this project, I implement a parking occupancy detection system for CCTV images. First, an object detection model is trained to detect the vehicles in the parking area. Then, the coordinates of individual parking slots are found by clustering the detected vehicles using spatio-temporal analysis. Lastly, a ResNet is used as a classifier to predict the occupancy within each parking slot. 

The detailed parking occupancy detection processes are listed below:

1. Feed multiple images of the whole parking area taken from different time into an object detection model as inputs
2. The objection model detects the cars in the images, then, outputs the bounding boxes of cars and their respective scores
3. Cluster the detected cars into individual parking slots by density-based clustering algorithm [11] which uses spatio-temporal analysis
4. Estimate the coordinates of the parking slots by weighing the coordinates of individual detection with the score of the detection in each cluster 
5. Improve the coordinates of the parking slots by statistics of the detections
6. Use the coordinates of the parking slots to crop the images of the whole parking area into multiple images of individual parking slot
7. Feed the images of individual parking slot into a classifier to predict if a parking slot is empty or occupied
8. Annotate the prediction results back to the original image of the whole parking area for visualisation



Please find more details in the report pdf file.
