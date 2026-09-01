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

Model| Average time|	Approx. FPS
YOLO11n|	~17.77 ms|	56.27 FPS
RT-DETR-L|	57.24 ms|	17.47 FPS

So, in this particular Colab/T4 test, YOLO11n is about 3.2× faster than RT-DETR-L.
```
