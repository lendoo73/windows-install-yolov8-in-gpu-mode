# Windows YOLOv8 GPU Mode

Windows examples for YOLOv8 detection, classification, segmentation, tracking, dataset preparation, and GPU training from the [YOLO Masterclass](https://www.udemy.com/course/yolo-masterclass-deep-learning-computer-vision-course/).

## Setup

1. Install a CUDA-enabled PyTorch build compatible with your NVIDIA GPU and driver using the [official PyTorch instructions](https://pytorch.org/get-started/locally/).
2. Create and activate a Python environment, then install this project's direct dependencies:

   ```powershell
   py -3.12 -m venv .venv
   .\.venv\Scripts\Activate.ps1
   python -m pip install --upgrade pip
   python -m pip install -r requirements.txt
   ```

3. Check that PyTorch can access the GPU:

   ```powershell
   python -c "import torch; print(torch.cuda.is_available())"
   ```

The project environment used Python 3.12.10, Ultralytics 8.4.103, and PyTorch 2.13.0+cu126. Use a PyTorch/CUDA combination supported by your installed driver; the exact version may differ by system.

## Datasets and training

The prepared face-mask, weather-classification, and coffee-leaf segmentation datasets and their YAML configurations are included under `data/`.

Train a model on the GPU with the included data:

```powershell
yolo classify train model=yolov8l-cls.pt data=data/classify/weather_dataset device=0 name=yolov8l-weather-classification
yolo segment train model=yolov8l-seg.pt data=data/segment/coffee-leaf.yaml device=0 name=yolov8_coffee_leaf
```

Official YOLO model weights such as `yolov8l.pt`, `yolov8l-cls.pt`, and `yolov8l-seg.pt` are not included; Ultralytics can download them when requested by name. The two retained custom-trained `last.pt` checkpoints are tracked with Git LFS:

- Weather classification: `runs/classify/yolov8l-weather-classification/weights/last.pt`
- Coffee-leaf segmentation: `runs/segment/yolov8_coffee_leaf/weights/last.pt`

The example inference media and other generated run outputs are not included. Supply your own image or video paths for prediction and tracking. The lesson-note Markdown files in the project root contain additional commands and examples.

## Dataset utilities

`split_dataset.py` splits images and matching YOLO labels into train, validation, and test folders. `split_dataset_class.py` splits images organized into class folders. `check_images.py` finds unreadable images and moves them to the destination specified with `--dest`.

See each script's command-line options with `python <script>.py --help`.
