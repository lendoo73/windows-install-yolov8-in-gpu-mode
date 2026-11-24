# 18-84. Windows : Perform training and see the accuracy graph using Tensorboard

Training a model:
```shell
yolo classify train \
    model=yolov8l-cls.pt \
    data=data/classify/weather_dataset \
    imgsz=224 \
    device=0 \
    workers=2 \
    batch=16 \
    epochs=100 \
    patience=50 \
    name=yolov8l-weather-classification
```

See the accuracy graph using Tensorboard:
```shell
tensorboard --logdir=runs/classify/yolov8l-weather-classification
```

Continue training from the last checkpoint:
```shell
yolo classify train \
    model=runs/classify/yolov8l-weather-classification/weights/last.pt \
    resume=True
```