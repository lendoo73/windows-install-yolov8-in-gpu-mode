# 14-63. Windows : Perform training and see the accuracy graph using Tensorboard

```shell
yolo detect train \
  model=yolov8l.pt \
  data=data/face_mask.yaml \
  imgsz=640 \
  workers=0 \
  batch=2 \
  epochs=300 \
  patience=50 \
  name=yolov8_face_mask
```

## See the training accuracy graph using Tensorboard

```shell
tensorboard --logdir=runs/detect/yolov8_face_mask
```

## 64. Windows : How to continue an unfinished training

```shell
yolo detect train \
  model=runs/detect/yolov8_face_mask/weights/last.pt \
  data=data/face_mask.yaml \
  resume=True
```