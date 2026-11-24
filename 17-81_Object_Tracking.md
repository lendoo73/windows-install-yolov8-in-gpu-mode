# 17-81. Object Tracking

Object tracking on a video using bounding boxes.
```shell
yolo track \
  model=yolov8l.pt \
  source=inference/kites.mp4 \
  show=True
```

Object tracking on a video using segmentation masks.
```shell
yolo track \
  model=yolov8l-seg.pt \
  source=inference/kites.mp4 \
  show=True
```

Object tracking on a trained model.
```shell
yolo track \
  model=runs/detect/yolo8_face_mask/weights/best.pt \
  source=inference/face-mask-video.mp4 \
  show=True
```