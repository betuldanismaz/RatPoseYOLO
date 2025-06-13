# RatPoseYOLO

## Description

This project demonstrates animal pose estimation using YOLOv8-Pose, focusing on a rat dataset. It includes data preparation, model training, visualization of results, and exporting the trained model.

## Key Features

*   **Pose Estimation:** Utilizes YOLOv8-Pose to detect and estimate keypoints on rats.
*   **Custom Dataset:** Train and test with a custom dataset containing rat images and keypoint annotations.
*   **Data Preparation:** Includes code for extracting frames from a video, converting annotations from XML format, and organizing data into the required YOLO format.
*   **Model Training:** Trains a YOLOv8-Pose model on the prepared dataset.
*   **Visualization:** Provides code to visualize predicted keypoints on test images.
*   **Model Export:** Exports the trained model to ONNX format.

## Usage

1.  **Prerequisites:**
    *   Google Colab environment.
    *   Install the required dependencies:
        ```bash
        pip install ultralytics
        ```

2.  **Data Preparation:**

    *   **[IMPORTANT]** Before running the notebook, you need to obtain a dataset of rat images with keypoint annotations in XML format (CVAT format).
    *   Modify the paths in the notebook (particularly in the "DATA PREPARATION" sections) to match the location of your dataset files on Google Drive.

3.  **Run the code:**

    *   Open the notebook (`yolo-pose-project.py` or similar).
    *   Connect to your Google Drive.
    *   Run the notebook cells sequentially. The notebook performs the following steps:
        *   **Mounts Google Drive**
        *   **Installs necessary packages**
        *   **(Conditional - DATA PREPARATION):**  This section extracts frames from video, converts data and moves the label files.  *Note: These cells can be skipped if data is already prepared.*
        *   **Train:** Sets up and trains the YOLOv8-Pose model.
        *   **Visualize:** Makes predictions using a sample image.
        *   **Inference:** Makes predictions on the test data.
        *   **Export:** Exports the trained model to ONNX format.

## Data Files

*   `/content/drive/MyDrive/cvat_pose_project/data.yaml`: YOLOv8 data configuration file.
*   `images/train`: Contains training images.
*   `images/test`: Contains test images.
*   `labels/train`: Contains training label files in YOLO format.
*   `labels/test`: Contains test label files in YOLO format.

## Model Training

*   The YOLOv8n-pose.pt pre-trained model is used as a starting point.
*   Training is performed using the Ultralytics YOLO library.

## Results and Visualization

*   The notebook saves prediction results (images with keypoints) in the `/content/runs/pose/predict` directory.
*   Code is provided to display example predictions.

## Model Export

*   The trained model is exported to ONNX format for wider compatibility and deployment.

## Disclaimer

This project requires a dataset of rat images with keypoint annotations, which is not included due to size and licensing restrictions. You will need to obtain or create your own dataset and adapt the data preparation code accordingly.
