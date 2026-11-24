# 86. Windows : Weather Classification

Classifying weather conditions on an image:
```shell
yolo classify predict \
    model=runs/classify/yolov8l-weather-classification/weights/last.pt \
    source=inference/classify/weather.png \
    save=True
```

Performing weather classification on a video:
```shell
yolo classify predict \
    model=runs/classify/yolov8l-weather-classification/weights/last.pt \
    source=inference/classify/weather-video.mp4 \
    show=True
```
