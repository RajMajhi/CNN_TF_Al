```
                    EXPERIMENT

          CNN                         Transformer
           │                               │
       YOLO11n                         RT-DETR-small & Large(just for checking the diff)
           │                               │
           └──────────────┬────────────────┘
                          │
                       Colab
                          │
                   Performance
                          │
                          ▼
                     Jetson Nano
                          │
              ┌───────────┴───────────┐
              ▼                       ▼
          CNN result             Transformer result


| Metric           |      YOLO11n |                RT-DETR-L |
| ---------------- | -----------: | -----------------------: |
| Architecture     | CNN-dominant | Transformer-based/hybrid |
| Parameters       |       2.62 M |                 2.15 M   |
| Model size       |    5.35 MB   |                 63.43 MB |
| GFLOPs           |        6.5   |                  105.7   |
| Measured latency |   17.77 ms   |               57.24 ms   |
| Measured FPS     |      56.27   |                  17.47   |


So, in this particular Colab/T4 test, YOLO11n is about 3.2× faster than RT-DETR-L.

COCO validation
     │
     ├───────────────┐
     │               │
     ▼               ▼
 YOLO11n          RT-DETR-L
     │               │
     ▼               ▼
 predictions      predictions
     │               │
     └───────┬───────┘
             ▼
       COCO ground truth
             │
             ▼
       ┌─────┼─────┐
       ▼     ▼     ▼
      mAP  Precision Recall

```
