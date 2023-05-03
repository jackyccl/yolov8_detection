# Yolo-v8 Football Players Detection
This is an application to detect football players using the latest Yolo-v8. Ultralytics YOLOv8 is the latest version of the YOLO (You Only Look Once) object detection and image segmentation model developed by Ultralytics.

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

For more information, please click [here](https://blog.roboflow.com/how-to-train-yolov8-on-a-custom-dataset/)
