# 17-78. Windows: Image Classification on image and video

Classification on an image.
```shell
yolo classify predict \
  model=yolov8l-cls.pt \
  source=inference/classify/bee.png \
  save=True
```

Classification on a video.
```shell
yolo classify predict \
  model=yolov8l-cls.pt \
  source=inference/classify/volleyball.mp4 \
  show=True
```