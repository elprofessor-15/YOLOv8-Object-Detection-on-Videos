YOLOv8 Object Detection on Videos

This repository demonstrates the use of the YOLOv8 model for real-time object detection in videos. The YOLOv8 model is one of the latest versions of the “You Only Look Once” (YOLO) family, known for its speed and accuracy in object detection tasks.

Overview

This project utilizes the pre-trained YOLOv8 model to detect and annotate objects in video frames. It processes input video files, applies object detection to each frame, and saves the annotated output video with bounding boxes and class labels.

Key features of this repository include:

	•	YOLOv8 Implementation: Leverages the powerful YOLOv8 model for detecting objects in dynamic visual data.
	•	Custom Video Support: Allows you to use any custom video of your choice as input.
	•	Frame-by-Frame Detection: The model processes each frame of the input video, detecting objects in real-time.
	•	Annotated Output Video: The output video is saved with bounding boxes and class labels over detected objects.
	•	Step-by-Step Guide: Includes a detailed tutorial on setting up the environment and running the model on any video input, making it beginner-friendly.
Usage

Running Object Detection on Videos

	1.	Prepare Your Input Video:
Ensure that the input video file is stored locally in the project directory. You can replace the sample video (traffic video.mp4) with any custom video of your choice.
	2.	Run the Detection:
The following code in the notebook will detect objects and save the output video with annotations:
# Load the YOLOv8 model

# Load the YOLOv8 model
model = torch.hub.load('ultralytics/yolov8', 'yolov8s', pretrained=True)

# Specify input and output video paths
input_video_path = '/path/to/your/input/video.mp4'
output_video_path = '/path/to/save/output_video_with_detections.mp4'

# Run detection and save the annotated output video
process_and_save_video(input_video_path, output_video_path)

# Specify input and output video paths
input_video_path = '/path/to/your/input/video.mp4'
output_video_path = '/path/to/save/output_video_with_detections.mp4'

# Run detection and save the annotated output video
process_and_save_video(input_video_path, output_video_path)

3.	Output:
The video is processed frame-by-frame, and objects are detected using the YOLOv8 model. The output video will contain bounding boxes around the detected objects, along with their class labels (e.g., “car”, “person”, etc.).

Custom Video Support

This project allows you to use any custom video as input. Simply update the input video path in the code with the path to your own video file:

input_video_path = '/path/to/your/custom/video.mp4'
Once updated, you can run the same pipeline to detect objects in your custom video.

Sample Results

Here’s an example of object detection on a sample traffic video:

Input Video:

Sample traffic video showing cars, pedestrians, and other objects in a dynamic urban scene.

Output Video:

	•	The output video contains the same traffic footage, but now annotated with bounding boxes and object class labels such as “car”, “person”, and “truck”.
	•	Bounding boxes are drawn around detected objects in real-time, showing YOLOv8’s high performance and accuracy in recognizing multiple objects in fast-changing frames.

Notebook

The implementation is provided as a Colab notebook (YOLOv8_Object_Detection.ipynb). The notebook includes:

	•	Loading the pre-trained YOLOv8 model.
	•	Frame-by-frame object detection in videos.
	•	Saving the annotated output video.
	•	Instructions to modify the input video and customize detection parameters.

You can run the notebook directly in Google Colab for a hands-on experience.

Custom Videos

One of the key features of this repository is its flexibility to run object detection on any custom video of your choice. Whether it’s a surveillance video, a drone footage, or a personal recording, you can easily apply the YOLOv8 model and obtain object detection results.

Steps to Apply on Custom Videos:

	1.	Upload your video to the project directory.
	2.	Update the input video path in the code.
	3.	Run the notebook or script to get the annotated video.

References

	•	YOLOv8 Documentation: https://www.researchgate.net/publication/377716736_YOLOv8-CAB_Improved_YOLOv8_for_Real-time_object_detection
	•	PyTorch Hub: For loading pre-trained models and additional PyTorch usage examples.
	•	Google Colab: To run the project on the cloud.
