# Helmet Detection using YOLOv8

This project uses YOLOv8 to detect helmets in images. It is trained on a custom dataset of bike images with and without helmets. The model can identify whether a person in the image is wearing a helmet or not.

## Dataset

The dataset used for training and validation is the **Helmet Detection Dataset**, which can be downloaded from Kaggle using the link below:

**Dataset Link:**  
[Helmet Detection Dataset on Kaggle](https://www.kaggle.com/datasets/andrewmvd/helmet-detection)

Once you've downloaded the dataset, unzip it and place the contents in the `datasets/helmet-detection` folder, which should contain two main directories:

- `annotations/` (containing XML annotation files)
- `images/` (containing PNG images)

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/helmet-detection.git
   cd helmet-detection
   ```

2. Install the necessary dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Organize your dataset directory as follows:

   ```
   datasets/
   └── helmet-detection/
       ├── images/
       │   ├── train/
       │   ├── val/
       │   └── test/
       ├── annotations/
       └── data.yaml
   ```

4. Modify `data.yaml` to point to your dataset directories (e.g., `train`, `val`, `test`).

5. To start training the model, run the following:
   ```bash
   python Model.py
   ```

## Model Details

- **Model**: YOLOv8
- **Dataset**: Helmet Detection Dataset from Kaggle
- **Training Epochs**: 5
- **Image Size**: 416x416
- **Batch Size**: 16

## Results

After training, the model achieved the following metrics on the validation set:

- **Precision**: 0.779
- **Recall**: 0.775
- **mAP@0.5**: 0.845
- **mAP@0.5:0.95**: 0.549

## License

This project is licensed under the MIT License.

## Acknowledgments

- The Helmet Detection Dataset is provided by [AndrewMVD on Kaggle](https://www.kaggle.com/datasets/andrewmvd/helmet-detection).
- YOLOv8 model by [Ultralytics](https://github.com/ultralytics/yolov8).
