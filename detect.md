## 12-46. Windows : YOLOv8 Object Detection on image

```shell
yolo detect predict model=yolov8l.pt source="https://ultralytics.com/images/bus.jpg" save=True

yolo detect predict model=yolov8l.pt source="inference/zebras.jpg" save=True conf=0.5 show=True

yolo detect predict model=yolov8l.pt source="inference" save=True conf=0.5 save_txt=True line_thickness=6

yolo detect predict \
  model=yolov8l.pt \
  source="https://thumbs.dreamstime.com/b/coach-giving-young-soccer-team-instructions-youth-football-team-coach-listening-briefing-coaching-kids-sports-87690428.jpg?w=992" \
  save=True \
  line_width=2
```

## 12-47. Windows : YOLOv8 Object Detection on video and webcam (GPU Mode)

```shell
yolo detect predict model=yolov8l.pt source="inference/kites.mp4" save=True show=True

yolo detect predict model=yolov8l.pt source=0 save=True show=True
```
