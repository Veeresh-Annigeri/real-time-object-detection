# Real-time-Object-Detection-by-using-OpenCV-and-YOLO
Detecting the multiple objects in images and real-time videos using the YOLO algorithm.

When it comes to object detection, popular detection frameworks are

* YOLO
* SSD
* Faster R-CNN
* Support for running YOLO/DarkNet has been added to OpenCV dnn module recently.

There are two approaches to Object detection and they are:
* Two-shot detection 
* Single-shot detection
In Two-shot detection method, there are two stages involved in this method. One is region proposal and then in the second stage, the classification of those regions and refinement of the location prediction takes place.

Single-shot detection skips the region proposal stage and yields final localization and content prediction at once. 
The YOLO algorithm(You Only Look Once), deals with object detection in a different way. It is a single-shot detector(SSD).
The biggest advantage of using YOLO is its super speed, it’s incredibly fast and can process 45 frames per second.


# Implementation of YOLO with OpenCV:
There are various implementations of YOLO algorithm and perhaps most popular of them is the Darknet. But here we used OpenCV to implement YOLO algorithm. Yolo can
be applied to image file, video file or also to webcam feed. To use YOLO via OpenCV, we need three files viz -[yoloV3.weights](https://pjreddie.com/media/files/yolov3.weights), [yoloV3.cfg](https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg) and “coco.names” . The “coco.names” file contains all the names of the labels on which this model has been trained on. First, to load the model using the function “cv2.dnn.ReadNet()”. This function loads the network into memory and automatically detects configuration and framework based on file name specified. After loading the model now either we used it to detects objects in an image or in sample video. We can even use it for real-time object detection.

# Results:
* Input Image1:
![office](https://user-images.githubusercontent.com/93006885/138569866-82142c0a-cf4e-4f77-9ac8-95a9394742a5.jpg)
* Output Image1:
![office_result](https://user-images.githubusercontent.com/93006885/138569849-c83afeb7-0c59-4242-a030-08a8a719f70c.jpg)
* Input Image2:
![test_image21](https://user-images.githubusercontent.com/93006885/138569947-2dd95cba-7ba7-4f4d-9b5e-1578fd63e7a3.jpg)
* Output Image2:
![test_image21_result](https://user-images.githubusercontent.com/93006885/138569940-8b26c651-f641-44f8-88ea-0b31d7c3bc42.jpg)



# Applications:
Object Detection is breaking into wide scope of enterprises, with use cases extending from individual security to efficiency in the working environment. Some of it’s applications in real life are as follows;
* TRACKING OBJECTS: Object tracking could also be used in tracking the motion of a ball during a match. In the field of traffic monitoring too object tracking plays a crucial role. It is needless to point out that in the field of security and surveillance object detection would play an even more important role. With object tracking it would be easier to track a person in a video.
* COUNTING THE CROWDS: Crowd counting or people counting is another significant application of object detection. During a big festival, or in a crowded mall this application comes in handy as it helps in dissecting the crowd and measure different groups. SELF-DRIVING CARS: Another unique application of object detection technique is definitely self-driving cars. A self-driving car can only navigate through a street safely if it could detect all the objects such as people, other cars, road signs on the road, in order to decide what action to take.
* DETECTING A VEHICLE: In a road full of speeding vehicles object detection can help in a big way by tracking a particular vehicle and even its number plate. So, if a car gets into an accident or, breaks traffic rules then it is easier to detect that particular car using object detection model and thereby decreasing the rate of crime while enhancing security.

# Limitation:
Arguably the largest limitation and drawback of the YOLO object detector is that:
It does not always handle small objects well
It especially does not handle objects grouped close together
The reason for this limitation is due to the YOLO algorithm itself:
The YOLO object detector divides an input image into an SxS grid where each cell in the grid predicts only a single object. If there exist multiple, small objects in a single cell then YOLO will be unable to detect them, ultimately leading to missed object detections.
