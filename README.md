# Real-time-Object-Detection-by-using-OpenCV-and-YOLO
Detecting the multiple objects in images and real-time videos using the YOLO algorithm.

When it comes to object detection, popular detection frameworks are

* YOLO
* SSD
* Faster R-CNN
* Support for running YOLO/DarkNet has been added to OpenCV dnn module recently.

# Implementation of YOLO with OpenCV:
There are various implementations of YOLO algorithm and perhaps most popular of them is the Darknet. But here we used OpenCV to implement YOLO algorithm. Yolo can
be applied to image file, video file or also to webcam feed. To use YOLO via OpenCV, we need three files viz -[yoloV3.weights](https://pjreddie.com/media/files/yolov3.weights), [yoloV3.cfg](https://github.com/pjreddie/darknet/blob/master/cfg/yolov3.cfg) and “coco.names” . The “coco.names” file contains all the names of the labels on which this model has been trained on. First, to load the model using the function “cv2.dnn.ReadNet()”. This function loads the network into memory and automatically detects configuration and framework based on file name specified. After loading the model now either we used it to detects objects in an image or in sample video. We can even use it for real-time object detection.

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
