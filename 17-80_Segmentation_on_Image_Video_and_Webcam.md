# 17-80. Segmentation on Image, Video, and Webcam

Segmentation on an image.
```shell
yolo segment predict \
  model=yolov8l-seg.pt \
  source=inference/zebras.jpg \
  save=True
```

Segmentation on a video.
```shell
yolo segment predict \
  model=yolov8l-seg.pt \
  source=inference/kites.mp4 \
  show=True
```

Segmentation on a webcam.
```shell
yolo segment predict \
  model=yolov8l-seg.pt \
  source=0 \
  show=True
```