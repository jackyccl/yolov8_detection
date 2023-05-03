# Yolo-v8 Football Players Detection
This is an application to detect football players using the latest Yolo-v8. Ultralytics YOLOv8 is the latest version of the YOLO (You Only Look Once) object detection and image segmentation model developed by Ultralytics.

# Demos
<img src="https://github.com/jackyccl/yolov8_detection/blob/main/demo_gifs/019d5b34_1_AdobeExpress.gif" width="480" height="270" />

<img src="https://github.com/jackyccl/yolov8_detection/blob/main/demo_gifs/08fd33_4_AdobeExpress.gif" width="480" height="270" />

Go to user interface demo at [here](https://app.roboflow.com/jackyccl/football-players-detection-2-e9a5j/overview).

## Preparing a custom dataset

We use RoboFlow to create custom datasets by following the steps below. 

### Step 1: Creating project in RoboFlow

### Step 2: Uploading images

We then add the data to the newly created project. We can drag and drop a directory with a dataset in RoboFlow dashboard.

### Step 3: Labeling

If there has only images, we can label them in [Roboflow Annotate](https://docs.roboflow.com/annotate).

### Step 4: Generate new dataset version

Now that we have our images and annotations added, we can generate a "dataset version". When generating a "Version", we may elect to add preprocessing and augmentations. This step is completely optional, however, it can allow you to significantly improve the robustness of your model.

### Step 5: Exporting dataset

Once the dataset version is generated, we have a hosted dataset we can load directly into our notebook for easy training. Click `Export` and select the `YOLO v8` dataset format.

### Step 6: Load Yolov8 CLI
Ultralytics released CLI and SDK version to train on our custom dataset. I use CLI in my training. Please refer the training procedures in the jupyter notebook. 

### Finish Training
The training logs can be found on the project [page](https://app.roboflow.com/jackyccl/football-players-detection-2-e9a5j/overview). We can directly test the model by accessing to the "Deploy" tab and simply upload an image for inference.

### Inference with videos
We can also test our model on a video with the following command:

`!yolo task=detect mode=predict model={HOME}/runs/detect/train/weights/best.pt conf=0.25 source={video_path}.mp4`
