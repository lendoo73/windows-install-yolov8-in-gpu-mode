# 15-73. YOLOv8: Accuracy Measurement using Mean Average Precision

```shell
yolo detect val \
    model=runs/detect/yolov8_face_mask/weights/best.pt \
    data=data/face_mask.yaml \
    device=0 \
    conf=0.01 \
    iou=0.5 \
    name=yolov8-face_mask-val
    split=val
```

Calculating the accuracy on test data.
```shell
yolo detect val \
    model=runs/detect/yolov8_face_mask/weights/best.pt \
    data=data/face_mask.yaml \
    device=0 \
    conf=0.01 \
    iou=0.5 \
    name=yolov8-face_mask-test
    split=test
```