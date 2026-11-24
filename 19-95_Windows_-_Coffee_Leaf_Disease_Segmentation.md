# 19-95. Windows : Coffee Leaf Disease Segmentation

Predicting the model:
```shell
yolo segment predict \
    model=runs/segment/yolov8_coffee_leaf/weights/best.pt \
    source=inference/coffee-leaf-disease.png \
    save=True
```