# 14-65. Windows : Face Mask Detection

Detecting face masks on images.
```shell
yolo detect predict \
  model=runs/detect/yolov8_face_mask/weights/best.pt \
  source=inference/face-mask.png \
  save=True
```

Detecting face masks on video.
```shell
yolo detect predict \
  model=runs/detect/yolov8_face_mask/weights/best.pt \
  source=inference/face-mask-video.mp4 \
  save=True \
  line_thickness=2
```