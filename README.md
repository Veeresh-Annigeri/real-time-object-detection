# Real-time-Object-Detection-by-using-OpenCV-and-YOLO
Detecting the multiple objects in images and real-time videos using the YOLO algorithm.

When it comes to object detection, popular detection frameworks are

* YOLO
* SSD
* Faster R-CNN
* Support for running YOLO/DarkNet has been added to OpenCV dnn module recently.

# Limitation:
Arguably the largest limitation and drawback of the YOLO object detector is that:
It does not always handle small objects well
It especially does not handle objects grouped close together
The reason for this limitation is due to the YOLO algorithm itself:
The YOLO object detector divides an input image into an SxS grid where each cell in the grid predicts only a single object. If there exist multiple, small objects in a single cell then YOLO will be unable to detect them, ultimately leading to missed object detections.
