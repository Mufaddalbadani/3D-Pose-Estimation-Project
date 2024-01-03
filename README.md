# 👯‍♂️ 2D-Pose-Estimation
Pose Estimation using OpenPose (Deep Learning with OpenCV)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

The objective of this project is to create a computer vision model that identifies key points related to human anatomy and establishes logical connections between these key points. The utilized model is a pre-trained OpenPose model developed by Carnegie Mellon University, generating two types of outputs: Confidence Maps and Part Affinity Maps. The code demonstration focuses on a single person in the image, employing Confidence Maps, also referred to as Probability Maps.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------- 

**Model**:- 
Open-Pose caffe model trained on multi purpose image dataset. The model is capable of detecting 135 keypoints.
Link to download the model :- https://www.dropbox.com/s/089r2yg6aao858l/opencv_bootcamp_assets_NB14.zip?dl=(URL)
The link contains a prototxt and caffe model file.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

**📖Project Overview**
The goal of the project is to develop a Deep Learning model to detect the keypoints and associate with the humans anatomy.

1. **Initialize Model and Load Pre-trained Weights**:- Install the model from the link above. It conatins a prototxt file and a caffe model file which is the model weights file.
2. **Define Pose Skeleton Structure**:- Specify the keypoints and their connections to form the pose skeleton (pose_parts).
3. **Image Input and Pre-processing**:- Read the input image (image) using OpenCV. Check if the image was successfully loaded
4. **Create Blob Representation**:- Prepare the image for the neural network by creating a blob representation | Use cv2.dnn.blobFromImage to normalize, resize, and organize the image for input to the neural network.
5. **Run Inference (Forward Pass)**:- Perform a forward pass to obtain the output, which includes probability maps for each keypoint.
6. **Post-process Probability Maps**:- Calculate the scaling factors (scaleX and scaleY) based on the original image and the output shape. | Set a probability threshold (threshold) to filter keypoint detections.
7. **Extract Keypoint Coordinates**:- Loop through the probability maps and identify the coordinates of keypoints based on the global maxima.
8. **Draw Keypoints on Image**:- Create a copy of the original image (imPoints) for visualization. | Draw circles at the detected keypoints and annotate them with keypoint indices.
9. **Draw Pose Skeleton**:- Create another copy of the original image (imSkeleton) for drawing the pose skeleton. | Connect keypoints with lines based on the specified skeleton structure. | Highlight keypoints with circles.
10. **Visualization and Interpretation**:-The visualization shows the detected keypoints and the pose skeleton on the original image.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

**🟢Notes**

* Ensure the proper setup of the pose model files (protofile and weightsfile).
* Adjust the threshold and other parameters based on specific project requirements.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Output**
![Asset 3](https://github.com/Mufaddalbadani/2D-Pose-Estimation/assets/62328487/3713f30c-8b3e-4593-bc81-95848ce86d85)
