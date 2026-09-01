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


| Metric                |       YOLO11n |      RT-DETR-L |
| --------------------- | ------------: | -------------: |
| Parameters            | **2,616,248** | **32,148,140** |
| Weight file           |   **5.35 MB** |   **63.43 MB** |
| Your measured FPS     |     **56.27** |      **17.47** |
| Your measured latency |  **17.77 ms** |   **57.24 ms** |

So, in this particular Colab/T4 test, YOLO11n is about 3.2× faster than RT-DETR-L.



```
