# 19-93. Windows : Perform training and see the accuracy graph using Tensorboard

Training the model:
```shell
yolo segment train \
    model=yolov8l-seg.pt \
    data=data/segment/coffee-leaf.yaml \
    imgsz=640 \
    workers=0 \
    batch=1 \
    device=0 \
    epochs=300 \
    patience=50 \
    name=yolov8_coffee_leaf
```

See the accuracy graph using Tensorboard:
```shell
tensorboard --logdir=runs/segment/yolov8_coffee_leaf
```

Continue training the model:
```shell
yolo segment train \
    model=runs/segment/yolov8_coffee_leaf/weights/last.pt \
    resume=True
```