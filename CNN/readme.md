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

1. Install Ultralytics
        ↓
2. Check GPU
        ↓
3. Import YOLO + RTDETR
        ↓
4. Load YOLO11n + RT-DETR-L
        ↓
5. Download/extract COCO
        ↓
6. Load COCO annotations
        ↓
7. Define JetAuto 15 classes
        ↓
8. Create JetAuto validation labels
        ↓
9. Create JetAuto training labels
        ↓
10. Create dataset YAML
        ↓
11. Fine-tune YOLO11n
        ↓
12. Fine-tune RT-DETR-L
        ↓
13. Evaluate both
        ↓
14. FPS / latency / memory
        ↓
15. Test on your own JetAuto video

```
