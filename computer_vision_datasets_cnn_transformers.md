# Computer Vision Datasets for CNNs and Transformers

This reference collects the major datasets commonly used to learn,
train, fine-tune, and benchmark **CNN-based, Vision Transformer
(ViT)-based, detection, segmentation, video, 3D, LiDAR, OCR,
vision-language, medical, and remote-sensing computer-vision models**.

The table is organized by **computer-vision task/domain** rather than by
model family. This is important because datasets such as **COCO,
ImageNet, KITTI, ADE20K, and Cityscapes are used by both CNN and
Transformer architectures**. For example, COCO is widely used for object
detection, instance segmentation, keypoints, captioning and related
tasks, while ImageNet is a major classification/pretraining benchmark.

### Download-link conventions

-   **Direct / public** = the download can normally be started without
    an account.
-   **Registration / request** = the official source requires
    registration, login, an application, or acceptance of terms.
-   **Kaggle / mirror** = an official or commonly used hosted copy is
    linked when the original source is gated.
-   Always check the dataset's license/terms before commercial use. Some
    datasets are restricted to research/education or require a separate
    license.

> **Note:** "Direct download" is not possible for every dataset.
> ImageNet, KITTI and several large research datasets require
> registration or acceptance of terms. The links below point to the
> official download page whenever a raw file URL is not publicly
> available.

------------------------------------------------------------------------

## 1. Image Classification

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset         Main task                      Approx. scale Typical CV use                Access                 Download
  --------------- ----------------------------- -------------- ----------------------------- ---------------------- -------------------------------------------------------------------------
  MNIST           Digit classification                     70K Beginner CNN, MLP             Direct                 [Download](http://yann.lecun.com/exdb/mnist/)

  Fashion-MNIST   Clothing classification                  70K CNN baseline                  Direct                 [Download](https://github.com/zalandoresearch/fashion-mnist#download)

  CIFAR-10        10-class image classification            60K CNN fundamentals              Direct                 [Download](https://www.cs.toronto.edu/~kriz/cifar.html)

  CIFAR-100       100-class image                          60K CNN/ViT                       Direct                 [Download](https://www.cs.toronto.edu/~kriz/cifar.html)
                  classification                                                                                    

  ImageNet-1K /   Classification/localization    1.4M+ indexed ResNet, ViT, Swin, ConvNeXt   Registration/request   [Official download](https://www.image-net.org/download.php)
  ILSVRC                                                subset                                                      

  ImageNet-21K    Large-scale classification             \~14M ViT/large-scale pretraining   Registration/request   [ImageNet](https://www.image-net.org/)

  Caltech-101     Object classification                   \~9K Transfer learning             Public                 [Dataset page](https://data.caltech.edu/records/mzrjq-6wc02)

  Caltech-256     Object classification                  \~30K Transfer learning             Public                 [Dataset page](https://data.caltech.edu/records/nyy15-4j048)

  Stanford Cars   Fine-grained car                       \~16K CNN/ViT fine-grained          Public/request         [Dataset page](https://ai.stanford.edu/~jkrause/cars/car_dataset.html)
                  classification                               recognition                                          

  Oxford-IIIT Pet Pet breed/species                     \~7.4K Classification/segmentation   Public                 [Download page](https://www.robots.ox.ac.uk/~vgg/data/pets/)

  CUB-200-2011    Fine-grained birds                     \~12K Fine-grained CNN/ViT          Public                 [Dataset page](https://www.vision.caltech.edu/datasets/cub_200_2011/)

  Food-101        Food classification                     101K Image classification          Public                 [Download](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/)

  Oxford          Flower classification                  8,189 Fine-grained recognition      Public                 [Download page](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/)
  Flowers-102                                                                                                       

  Describable     Texture classification                 5,640 Texture recognition           Public                 [Download](https://www.robots.ox.ac.uk/~vgg/data/dtd/)
  Textures (DTD)                                                                                                    

  Places365       Scene classification                Millions Scene recognition/pretraining Registration/request   [Dataset](http://places2.csail.mit.edu/download.html)
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 2. Object Detection

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Main task                  Approx. scale Typical models/use  Access                 Download
  ------------ ------------------------ --------------- ------------------- ---------------------- -------------------------------------------------------------------
  COCO 2017    Object detection,            330K images YOLO, Faster R-CNN, Direct                 [COCO download](https://cocodataset.org/#download)
               segmentation, keypoints,                 DETR, DINO                                 
               captions                                                                            

  Pascal VOC   Object                      \~20K images R-CNN, Faster       Direct                 [VOC download](http://host.robots.ox.ac.uk/pascal/VOC/)
  2007/2012    detection/segmentation                   R-CNN, YOLO                                

  Open Images  Detection,                   \~9M images Large-scale         Public                 [Open
               classification,                          detection                                  Images](https://storage.googleapis.com/openimages/web/index.html)
               segmentation                                                                        

  Objects365   Large-scale object           \~2M images YOLO/DETR           Registration/request   [Dataset](https://www.objects365.org/)
               detection                                pretraining                                

  LVIS         Long-tail                   100K+ images Mask                Public/request         [LVIS](https://www.lvisdataset.org/)
               detection/instance                       R-CNN/Transformer                          
               segmentation                                                                        

  WIDER FACE   Face detection              \~32K images Face detectors      Public                 [Download](http://shuoyang1213.me/WIDERFACE/)

  CrowdHuman   Human detection             \~15K images Dense/crowded       Public                 [Download](https://www.crowdhuman.org/)
                                                        detection                                  

  VisDrone     Drone detection/tracking            10K+ YOLO/DETR           Public                 [Download](https://github.com/VisDrone/VisDrone-Dataset)
                                          images/videos                                            

  DOTA         Aerial object detection     2,800+ large Oriented detection  Public                 [Download](https://captain-whu.github.io/DOTA/)
                                                 images                                            

  UAVDT        UAV vehicle              Video sequences Drone perception    Public                 [Download](https://sites.google.com/view/daweidu/projects/uavdt)
               detection/tracking                                                                  

  UA-DETRAC    Vehicle                       100 videos Vehicle detection   Public                 [Dataset](http://detrac-db.rit.albany.edu/)
               detection/tracking                                                                  

  BDD100K      Driving perception                  100K YOLO/DETR, driving  Public                 [Download](https://bdd-data.berkeley.edu/)
                                          videos/images CV                                         

  KITTI Object 2D/3D detection               7.5K train 3D detection        Registration           [Download](https://www.cvlibs.net/datasets/kitti/eval_object.php)
                                                 images                                            

  Waymo Open   2D/3D detection              Large-scale 3D CNN/Transformer  Registration           [Download](https://waymo.com/open/)
  Dataset                                       driving                                            

  nuScenes     3D detection                1,000 scenes BEV/3D Transformer  Registration           [Download](https://www.nuscenes.org/download)
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 3. Semantic Segmentation

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Main task                    Approx. scale Typical use             Access         Download
  ------------ -------------------------- --------------- ----------------------- -------------- ------------------------------------------------------------------------------------------------
  PASCAL VOC   Semantic/instance                    \~20K FCN, DeepLab, Mask      Direct         [VOC](http://host.robots.ox.ac.uk/pascal/VOC/)
               segmentation                               R-CNN                                  

  COCO-Stuff   Semantic/stuff                  COCO-scale CNN/Transformer         Public         [COCO](https://cocodataset.org/#download)
               segmentation                               segmentation                           

  Cityscapes   Urban semantic              5K fine images DeepLab, SegFormer,     Registration   [Download](https://www.cityscapes-dataset.com/downloads/)
               segmentation                               driving                                

  ADE20K       Scene parsing/segmentation   27K train/val SegFormer, Mask2Former, Registration   [Download](https://ade20k.csail.mit.edu/)
                                                          Swin                                   

  CamVid       Road-scene segmentation         701 images Segmentation basics     Public         [Download](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/)

  Mapillary    Street-scene segmentation       25K images Autonomous driving      Registration   [Download](https://www.mapillary.com/dataset/vistas)
  Vistas                                                                                         

  BDD100K      Driving segmentation                  100K Driving perception      Public         [Download](https://bdd-data.berkeley.edu/)
                                            videos/images                                        

  KITTI        Road/3D perception                 Driving Segmentation/depth/3D   Registration   [Download](https://www.cvlibs.net/datasets/kitti/)
                                                sequences                                        

  SUN RGB-D    Indoor RGB-D segmentation       10K images Indoor scene            Public         [Download](http://rgbd.cs.princeton.edu/)
                                                          understanding                          

  NYU Depth V2 RGB-D/depth/segmentation     1,449 labeled Depth/segmentation      Public         [Download](https://cs.nyu.edu/~fergus/datasets/nyu_depths.html)
                                                   frames                                        

  ISPRS        Aerial segmentation         38 large tiles Remote sensing          Public         [Download](https://www.isprs.org/education/benchmarks/UrbanSemLab/2d-sem-label-potsdam.aspx)
  Potsdam                                                                                        

  ISPRS        Aerial segmentation               33 tiles Remote sensing          Public         [Download](https://www.isprs.org/education/benchmarks/UrbanSemLab/2d-sem-label-vaihingen.aspx)
  Vaihingen                                                                                      

  LoveDA       Land-cover segmentation       5,987 images Remote sensing          Public         [Download](https://github.com/Junjue-Wang/LoveDA)

  Pascal       Scene parsing                        \~10K Semantic segmentation   Public         [Dataset](https://cs.stanford.edu/~roozbeh/pascal-context/)
  Context                                                                                        
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 4. Instance and Panoptic Segmentation

  ---------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset       Task                       Approx. scale Typical models      Access           Download
  ------------- ------------------------- -------------- ------------------- ---------------- -------------------------------------------------------------
  COCO Instance Instance segmentation               COCO Mask R-CNN, SOLO,   Direct           [COCO](https://cocodataset.org/#download)
                                                         Mask2Former                          

  COCO Panoptic Panoptic segmentation               COCO Panoptic FPN,       Direct           [COCO](https://cocodataset.org/#download)
                                                         Mask2Former                          

  LVIS          Long-tail instance                 100K+ Mask                Public/request   [LVIS](https://www.lvisdataset.org/)
                segmentation                             R-CNN/Mask2Former                    

  Cityscapes    Instance/panoptic                     5K Mask                Registration     [Cityscapes](https://www.cityscapes-dataset.com/downloads/)
                                                         R-CNN/Transformer                    

  ADE20K        Semantic/panoptic/scene              27K Mask2Former/Swin    Registration     [ADE20K](https://ade20k.csail.mit.edu/)
                parsing                                                                       

  Mapillary     Instance/semantic                    25K Driving             Registration     [Mapillary](https://www.mapillary.com/dataset/vistas)
  Vistas        segmentation                             segmentation                         

  YouTube-VOS   Video object segmentation     4K+ videos Video segmentation  Public           [Download](https://youtube-vos.org/)

  DAVIS         Video object segmentation    150+ videos VOS                 Public           [Download](https://davischallenge.org/)
  ---------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 5. Face Datasets

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset         Task                           Approx. scale Typical use                Access            Download
  --------------- ----------------------------- -------------- -------------------------- ----------------- ----------------------------------------------------------------------------------------------------------------------------
  WIDER FACE      Face detection                  \~32K images Detection                  Public            [Download](http://shuoyang1213.me/WIDERFACE/)

  LFW             Face verification                13K+ images Recognition/verification   Public            [Download](http://vis-www.cs.umass.edu/lfw/)

  CelebA          Face attributes                  200K images Attributes/detection       Public            [Download](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)

  CelebA-HQ       High-quality faces                       30K Generative/face models     Public            [Dataset](https://github.com/tkarras/progressive_growing_of_gans)

  VGGFace2        Face recognition                 3.3M images Face recognition           Request           [Dataset](https://www.robots.ox.ac.uk/~vgg/data/vgg_face2/)

  CASIA-WebFace   Face recognition                      \~500K Recognition                Public/research   [Dataset](http://www.cbsr.ia.ac.cn/english/CASIA-WebFace-Database.html)

  MegaFace        Large-scale face recognition        Millions Recognition benchmark      Registration      [Dataset](http://megaface.cs.washington.edu/)

  IJB-A/B/C       Face                             Large-scale Recognition                Request           [NIST IJB](https://www.nist.gov/programs-projects/face-challenges)
                  verification/identification        benchmark                                              

  MS1M            Face recognition                    Millions Face recognition training  Research access   [MS-Celeb-1M](https://www.microsoft.com/en-us/research/project/ms-celeb-1m-challenge-recognizing-one-million-celebrities/)
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 6. Human Pose / Keypoints

  --------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Task           Approx. scale Typical models    Access           Download
  ------------ ------------- -------------- ----------------- ---------------- ---------------------------------------------------------------
  COCO         2D human pose   COCO persons HRNet, ViTPose    Direct           [COCO](https://cocodataset.org/#download)
  Keypoints                                                                    

  MPII Human   Human pose      \~25K images CNN/Transformer   Public           [Download](http://human-pose.mpi-inf.mpg.de/)
  Pose                                      pose                               

  Human3.6M    3D human pose    Large video 3D pose           Request          [Dataset](http://vision.imar.ro/human3.6m/description.php)
                                    dataset                                    

  PoseTrack    Video pose             Video Pose tracking     Public/request   [Download](https://posetrack.net/)
               tracking           sequences                                    

  CrowdPose    Crowded pose    \~20K images Pose estimation   Public           [Download](https://github.com/Jeff-sjtu/CrowdPose)
               estimation                                                      

  AI           Human pose       Large-scale Pose estimation   Public           [Dataset](https://github.com/AIChallenger/AI_Challenger_2017)
  Challenger                                                                   

  Penn Action  Pose/action        2K videos Pose + action     Public           [Download](http://dreamdragon.github.io/PennAction/)
  --------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 7. Autonomous Driving / Multi-Sensor Vision

  ----------------------------------------------------------------------------------------------------------------------------------------------
  Dataset       Sensors        Main tasks               Scale /          Access            Download
                                                        characteristic                     
  ------------- -------------- ------------------------ ---------------- ----------------- -----------------------------------------------------
  KITTI         Camera +       2D/3D detection,         Classic driving  Registration      [KITTI](https://www.cvlibs.net/datasets/kitti/)
                LiDAR + GPS    tracking, depth,         benchmark                          
                               odometry                                                    

  nuScenes      6 cameras +    3D detection, tracking,  1,000 scenes     Registration      [nuScenes](https://www.nuscenes.org/download)
                LiDAR + 5      prediction                                                  
                radar +                                                                    
                GPS/IMU                                                                    

  Waymo Open    Camera + LiDAR 2D/3D detection,         Large-scale      Registration      [Waymo](https://waymo.com/open/)
  Dataset                      tracking                 autonomous                         
                                                        driving                            

  Argoverse     Camera + LiDAR 3D detection, tracking,  Urban driving    Registration      [Argoverse](https://www.argoverse.org/)
                               forecasting                                                 

  Lyft Level 5  Camera + LiDAR 3D detection             Autonomous       Public/research   [Dataset](https://level-5.global/)
                                                        driving                            

  ONCE          Camera + LiDAR 3D detection             Large-scale      Public            [Dataset](https://once-for-auto-driving.github.io/)
                                                        LiDAR                              

  PandaSet      Camera + LiDAR 3D                       100+ driving     Public            [Dataset](https://scale.com/open-datasets/pandaset)
                               detection/segmentation   scenes                             

  A2D2          Camera +       Detection/segmentation   Audi autonomous  Public            [Dataset](https://www.a2d2.audi/a2d2/en.html)
                LiDAR + radar                           driving                            

  ApolloScape   Camera + LiDAR Driving perception       Urban driving    Public/research   [Dataset](http://apolloscape.auto/)

  BDD100K       Camera/video   Detection, tracking,     100K driving     Public            [BDD100K](https://bdd-data.berkeley.edu/)
                               lane, segmentation       videos                             

  Cityscapes    Stereo camera  Segmentation, detection  European urban   Registration      [Cityscapes](https://www.cityscapes-dataset.com/)
                                                        scenes                             
  ----------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 8. LiDAR / Point-Cloud / 3D Vision

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset             Modality    Task                          Typical models            Access           Download
  ------------------- ----------- ----------------------------- ------------------------- ---------------- ----------------------------------------------------------------
  KITTI 3D            LiDAR +     3D detection                  PointPillars, PV-RCNN,    Registration     [KITTI](https://www.cvlibs.net/datasets/kitti/eval_object.php)
                      camera                                    VoxelNet                                   

  nuScenes-LidarSeg   LiDAR       Semantic segmentation         Point/voxel/Transformer   Registration     [Download](https://www.nuscenes.org/download)

  SemanticKITTI       LiDAR       Semantic/sequence             PointNet++, Minkowski,    Public           [Download](http://www.semantic-kitti.org/dataset.html)
                                  segmentation                  Transformer                                

  Waymo Open Dataset  LiDAR +     3D detection/segmentation     3D CNN/Transformer        Registration     [Waymo](https://waymo.com/open/)
                      camera                                                                               

  ONCE                LiDAR +     3D detection                  LiDAR Transformers        Public           [ONCE](https://once-for-auto-driving.github.io/)
                      camera                                                                               

  PandaSet            LiDAR +     3D detection/segmentation     3D perception             Public           [PandaSet](https://scale.com/open-datasets/pandaset)
                      camera                                                                               

  A2D2                LiDAR +     3D perception                 Autonomous driving        Public           [A2D2](https://www.a2d2.audi/a2d2/en.html)
                      camera                                                                               

  ScanNet             RGB-D       3D scene understanding        3D segmentation           Registration     [ScanNet](http://www.scan-net.org/)

  S3DIS               3D point    Indoor semantic segmentation  PointNet/Point            Public           [Download](http://buildingparser.stanford.edu/dataset.html)
                      clouds                                    Transformer                                

  ShapeNet            3D meshes   Shape                         3D deep learning          Registration     [ShapeNet](https://shapenet.org/)
                                  classification/segmentation                                              

  ModelNet40          3D objects  Classification                PointNet/Point            Public           [Download](https://modelnet.cs.princeton.edu/)
                                                                Transformer                                

  SUN RGB-D           RGB-D       3D detection/segmentation     RGB-D models              Public           [Download](http://rgbd.cs.princeton.edu/)

  Matterport3D        RGB-D/3D    Indoor scene understanding    3D segmentation           Request          [Dataset](https://niessner.github.io/Matterport/)

  PartNet             3D shapes   Part segmentation             3D Transformer            Public/request   [Dataset](https://partnet.cs.stanford.edu/)

  Objaverse           3D objects  3D pretraining/generation     3D foundation models      Public           [Objaverse](https://objaverse.allenai.org/)
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 9. Optical Flow

  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset          Task                 Scale Typical models    Access         Download
  ---------------- ----------- -------------- ----------------- -------------- -------------------------------------------------------------------------------------------------
  FlyingChairs     Optical          22K image FlowNet, RAFT     Public         [Download](https://lmb.informatik.uni-freiburg.de/resources/datasets/FlyingChairs.en.html)
                   flow                 pairs                                  

  FlyingThings3D   Optical          Synthetic Flow/scene flow   Public         [Download](https://lmb.informatik.uni-freiburg.de/resources/datasets/SceneFlowDatasets.en.html)
                   flow/3D                                                     
                   motion                                                      

  Sintel           Optical          Synthetic RAFT/FlowFormer   Public         [Download](http://sintel.is.tue.mpg.de/)
                   flow                 movie                                  

  KITTI Flow       Optical            Driving Flow estimation   Registration   [KITTI](https://www.cvlibs.net/datasets/kitti/eval_scene_flow.php)
                   flow                                                        

  HD1K             Optical            Driving Optical flow      Public         [Download](http://hciweb2.iwr.uni-heidelberg.de/vislearn/HD1K/)
                   flow                                                        

  Middlebury       Optical              Small Flow estimation   Public         [Download](https://vision.middlebury.edu/flow/)
                   flow             benchmark                                  
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 10. Video Understanding / Action Recognition

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset               Task                                Scale Typical models         Access            Download
  --------------------- -------------------------- -------------- ---------------------- ----------------- -----------------------------------------------------------------------------------------------------------
  UCF101                Action recognition             13K videos CNN/RNN/Video          Public            [Download](https://www.crcv.ucf.edu/data/UCF101.php)
                                                                  Transformer                              

  HMDB51                Action recognition              7K videos Video classification   Public            [Download](https://serre-lab.clps.brown.edu/resource/hmdb-a-large-human-motion-database/)

  Kinetics-400          Action recognition            400 classes TimeSformer, Video     Video URLs/terms  [Dataset](https://deepmind.google/discover/blog/kinetics-700-a-new-dataset-for-human-action-recognition/)
                                                                  Swin                                     

  Kinetics-600          Action recognition            600 classes Video Transformers     Video URLs/terms  [Dataset](https://github.com/cvdfoundation/kinetics-dataset)

  Kinetics-700          Action recognition            700 classes Video Transformers     Video URLs/terms  [Dataset](https://github.com/cvdfoundation/kinetics-dataset)

  Something-Something   Fine-grained actions          220K videos Video Transformers     Registration      [Download](https://developer.qualcomm.com/software/ai-datasets/something-something)
  V2                                                                                                       

  AVA                   Spatiotemporal action         Video clips Action Transformer     Public/research   [Download](https://research.google.com/ava/)
                        detection                                                                          

  ActivityNet           Activity                       20K videos Video understanding    Public            [Download](http://activity-net.org/)
                        recognition/localization                                                           

  Charades              Human activities               10K videos Video recognition      Public            [Download](https://prior.allenai.org/projects/charades)

  YouTube-8M            Video classification          Millions of Video representation   Public features   [Download](https://research.google.com/youtube8m/)
                                                           videos learning                                 

  MOT17                 Multi-object tracking          7 training Tracking               Public            [Download](https://motchallenge.net/data/MOT17/)
                                                        sequences                                          

  MOT20                 Crowded tracking              8 sequences Tracking/Transformer   Public            [Download](https://motchallenge.net/data/MOT20/)
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 11. Vision-Language / Image-Text / VQA

  ------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Task                   Approx. scale Typical models           Access            Download
  ------------ --------------------- -------------- ------------------------ ----------------- ---------------------------------------------------------------
  COCO         Image captioning         330K images CNN/Transformer/VLM      Direct            [COCO](https://cocodataset.org/#download)
  Captions                                                                                     

  Flickr30k    Image-text                31K images CLIP-style/VLM           Public/research   [Dataset](https://shannon.cs.illinois.edu/DenotationGraph/)
               matching/captioning                                                             

  Conceptual   Image-text                  Millions Vision-language          Public URLs       [Dataset](https://ai.google.com/research/ConceptualCaptions/)
  Captions     pretraining                                                                     

  Visual       Objects, attributes,     108K images VLM/scene graphs         Public            [Download](https://visualgenome.org/)
  Genome       relationships                                                                   

  VQA v2       Visual question         200K+ images VQA Transformer          Public            [Download](https://visualqa.org/download.html)
               answering                                                                       

  GQA          Visual reasoning       22M questions VLM/reasoning            Public            [Download](https://cs.stanford.edu/people/dorarad/gqa/)

  NLVR2        Vision-language       100K+ examples Multimodal Transformers  Public            [Download](https://lil.nlp.cornell.edu/nlvr/)
               reasoning                                                                       

  TextVQA      Text-based VQA         45K questions OCR/VLM                  Public            [Download](https://textvqa.org/)

  OK-VQA       Knowledge-based VQA    14K questions VLM/reasoning            Public            [Download](https://okvqa.allenai.org/)

  RefCOCO      Referring expressions    19K+ images Grounding/segmentation   Public            [Dataset](https://github.com/lichengunc/refer)

  RefCOCO+     Referring expressions   \~19K images Grounding                Public            [Dataset](https://github.com/lichengunc/refer)

  RefCOCOg     Referring expressions   \~26K images Grounding                Public            [Dataset](https://github.com/lichengunc/refer)
  ------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 12. OCR / Scene Text / Documents

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Task                             Scale Typical models    Access            Download
  ------------ ----------------------- -------------- ----------------- ----------------- -------------------------------------------------------------------------------------------
  EMNIST       Character recognition            800K+ CNN/ViT           Direct            [Download](https://www.nist.gov/itl/products-and-services/emnist-dataset)

  SVHN         Street-number                    600K+ CNN               Public            [Download](http://ufldl.stanford.edu/housenumbers/)
               recognition                                                                

  ICDAR        Scene text                    Multiple OCR/Transformer   Public/research   [Dataset hub](https://rrc.cvc.uab.es/)
               detection/recognition       challenges                                     

  SynthText /  Synthetic text             \~9M images OCR pretraining   Public            [Download](https://www.robots.ox.ac.uk/~vgg/data/text/)
  MJSynth                                                                                 

  IIIT5K       Scene text                   5K images OCR               Public            [Dataset](https://cvit.iiit.ac.in/research/projects/cvit-projects/scene-text-recognition)

  Total-Text   Curved text detection     1,555 images Text detection    Public            [Dataset](https://github.com/cs-chan/Total-Text-Dataset)

  COCO-Text    Text in natural images    COCO-derived OCR/text          Public            [Dataset](https://bgshih.github.io/cocotext/)
                                                      detection                           

  FUNSD        Form understanding       199 documents Document AI       Public            [Download](https://guillaumejaume.github.io/FUNSD/)

  SROIE        Receipt understanding   1,000 receipts OCR/document AI   Public            [Dataset](https://rrc.cvc.uab.es/?ch=13)

  DocVQA       Document VQA             50K questions Document          Public            [Download](https://www.docvqa.org/)
                                                      Transformer                         

  PubLayNet    Document layout                  360K+ Layout detection  Public            [Dataset](https://github.com/ibm-aur-nlp/PubLayNet)
                                            documents                                     

  RVL-CDIP     Document classification    400K images Document          Public            [Dataset](https://www.cs.cmu.edu/~aharley/rvl-cdip/)
                                                      classification                      
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 13. Medical Computer Vision

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset        Domain       Task                          Typical models      Access         Download
  -------------- ------------ ----------------------------- ------------------- -------------- ----------------------------------------------------------------------
  ISIC           Skin lesions Classification/segmentation   CNN/ViT             Public         [ISIC Archive](https://www.isic-archive.com/)

  HAM10000       Dermoscopy   Skin-lesion classification    CNN/ViT             Public         [Dataset](https://www.nature.com/articles/sdata2018161)

  CheXpert       Chest X-ray  Classification                CNN/ViT             Registration   [Download](https://stanfordmlgroup.github.io/competitions/chexpert/)

  NIH            Chest X-ray  Multi-label classification    CNN/ViT             Public         [Download](https://nihcc.app.box.com/v/ChestXray-NIHCC)
  ChestX-ray14                                                                                 

  MIMIC-CXR      Chest X-ray  Classification/reporting      Medical VLM         Credentialed   [Dataset](https://physionet.org/content/mimic-cxr/)
                                                                                access         

  BraTS          Brain MRI    Tumor segmentation            U-Net/Transformer   Registration   [Download](https://www.med.upenn.edu/cbica/brats2021/)

  LUNA16         Lung CT      Nodule detection              3D CNN              Public         [Download](https://luna16.grand-challenge.org/)

  KiTS           Kidney CT    Segmentation                  3D CNN/Transformer  Public         [Dataset](https://kits-challenge.org/)

  ACDC           Cardiac MRI  Segmentation                  U-Net/Transformer   Public         [Download](https://www.creatis.insa-lyon.fr/Challenge/acdc/)

  DRIVE          Retinal      Vessel segmentation           U-Net/CNN           Public         [Download](https://drive.grand-challenge.org/)
                 images                                                                        

  STARE          Retinal      Vessel segmentation           CNN                 Public         [Dataset](https://cecas.clemson.edu/~ahoover/stare/)
                 images                                                                        

  EyePACS        Retinal      Diabetic retinopathy          CNN/ViT             Kaggle         [Kaggle
                 images                                                                        dataset](https://www.kaggle.com/c/diabetic-retinopathy-detection)
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 14. Remote Sensing / Satellite Vision

  -----------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset       Task                       Scale Typical use              Access      Download
  ------------- ----------------- -------------- ------------------------ ----------- -----------------------------------------------------------------------
  DOTA          Aerial object       2,800+ large Oriented detection       Public      [DOTA](https://captain-whu.github.io/DOTA/)
                detection                 images                                      

  xView         Satellite object    \~1M objects Detection                Public      [Download](http://xviewdataset.org/)
                detection                                                             

  DIOR          Remote-sensing        23K images Object detection         Public      [Dataset](https://gcheng-nwpu.github.io/#Datasets)
                detection                                                             

  NWPU VHR-10   Aerial detection      800 images Detection                Public      [Dataset](http://www.escience.cn/people/gongcheng/NWPU-VHR-10.html)

  LoveDA        Land-cover          5,987 images Segmentation             Public      [GitHub](https://github.com/Junjue-Wang/LoveDA)
                segmentation                                                          

  SpaceNet      Buildings/roads            Large Segmentation/detection   Public      [Dataset](https://spacenet.ai/)
                                       satellite                                      
                                         imagery                                      

  DeepGlobe     Satellite            Large-scale Land/road/building       Public      [Dataset](http://deepglobe.org/)
                segmentation                     segmentation                         

  BigEarthNet   Sentinel-2 land    590K+ patches Multi-label              Public      [Download](https://bigearth.net/)
                cover                            classification                       

  EuroSAT       Satellite             27K images CNN/ViT classification   Public      [Download](https://github.com/phelber/eurosat)
                classification                                                        

  RESISC45      Remote-sensing      31.5K images Scene classification     Public      [Dataset](http://www.escience.cn/people/JunweiHan/NWPU-RESISC45.html)
                scenes                                                                
  -----------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 15. Depth Estimation

  -------------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Task               Modality             Typical models Access            Download
  ------------ ------------------ -------------------- -------------- ----------------- -----------------------------------------------------------------
  NYU Depth V2 Monocular/indoor   RGB-D                DPT, Depth     Public            [Download](https://cs.nyu.edu/~fergus/datasets/nyu_depths.html)
               depth                                   Anything                         

  KITTI Depth  Outdoor depth      Stereo/LiDAR         Monocular      Registration      [KITTI](https://www.cvlibs.net/datasets/kitti/eval_depth.php)
                                                       depth                            

  Middlebury   Stereo/depth       Stereo               Stereo         Public            [Dataset](https://vision.middlebury.edu/stereo/)
                                                       matching                         

  Make3D       Outdoor depth      RGB + depth          Depth          Public            [Dataset](http://make3d.cs.cornell.edu/)
                                                       estimation                       

  ScanNet      Indoor depth       RGB-D                3D/depth       Registration      [ScanNet](http://www.scan-net.org/)

  ETH3D        Stereo/3D          Stereo               Depth/stereo   Public            [Download](https://www.eth3d.net/)

  Hypersim     Synthetic indoor   RGB-D                Depth/3D       Public            [Dataset](https://github.com/apple/ml-hypersim)
               depth                                                                    

  DDAD         Driving depth      Multi-camera/LiDAR   Depth/3D       Public/research   [Dataset](https://github.com/TRI-ML/DDAD)

  DIML Indoor  Indoor depth       RGB-D                Depth          Public            [Dataset](https://dimlrgbd.github.io/)
                                                       estimation                       
  -------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## 16. 3D Shape / Object Understanding

  -------------------------------------------------------------------------------------------------------------------------------------------------
  Dataset      Task                      Scale Typical models           Access           Download
  ------------ ---------------- -------------- ------------------------ ---------------- ----------------------------------------------------------
  ModelNet10   3D                   10 classes PointNet/3D CNN          Public           [Download](https://modelnet.cs.princeton.edu/)
               classification                                                            

  ModelNet40   3D                   40 classes PointNet/Point           Public           [Download](https://modelnet.cs.princeton.edu/)
               classification                  Transformer                               

  ShapeNet     3D shape            Large-scale PointNet/3D Transformer  Registration     [ShapeNet](https://shapenet.org/)
               understanding                                                             

  ScanNet      3D scene           1,500+ scans 3D                       Registration     [ScanNet](http://www.scan-net.org/)
               understanding                   segmentation/detection                    

  S3DIS        Indoor                  6 areas PointNet/Point           Public           [S3DIS](http://buildingparser.stanford.edu/dataset.html)
               point-cloud                     Transformer                               
               segmentation                                                              

  SUN RGB-D    RGB-D 3D             10K images 3D detection             Public           [SUN RGB-D](http://rgbd.cs.princeton.edu/)
               understanding                                                             

  PartNet      3D part             Large-scale 3D part models           Public/request   [PartNet](https://partnet.cs.stanford.edu/)
               segmentation                                                              

  Objaverse    3D object        Millions of 3D 3D foundation models     Public           [Objaverse](https://objaverse.allenai.org/)
               collection               assets                                           
  -------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

# 17. Recommended Dataset Progression for Learning CNN → Transformer CV

If your goal is to understand the evolution of computer vision rather
than simply collect datasets, this is a practical order:

  Stage   Dataset               What to learn
  ------- --------------------- -----------------------------------------
  1       MNIST                 Tensors, images, training loop
  2       CIFAR-10              CNN, convolution, pooling, augmentation
  3       CIFAR-100             Deeper CNNs and transfer learning
  4       ImageNet-1K           ResNet, EfficientNet, ConvNeXt, ViT
  5       Pascal VOC            Bounding boxes and early detection
  6       COCO                  Modern detection + segmentation
  7       COCO Keypoints        Human pose
  8       ADE20K                Semantic segmentation
  9       Cityscapes            Real-world scene understanding
  10      Kinetics              Video Transformers
  11      KITTI                 3D perception
  12      nuScenes              Multi-sensor BEV/3D Transformers
  13      SemanticKITTI         LiDAR segmentation
  14      Visual Genome / VQA   Vision-language models

------------------------------------------------------------------------

# 18. Most Important Datasets to Know

If you don't want to work through the entire list immediately,
prioritize these:

**Classification** - MNIST - CIFAR-10 - CIFAR-100 - ImageNet-1K

**Detection** - Pascal VOC - COCO - Open Images - Objects365 - LVIS

**Segmentation** - COCO - Cityscapes - ADE20K - Mapillary Vistas

**Pose** - COCO Keypoints - MPII

**Video** - UCF101 - Kinetics-400/600/700 - Something-Something V2

**3D / Autonomous Driving** - KITTI - nuScenes - Waymo - SemanticKITTI

**Vision-Language** - COCO Captions - Visual Genome - VQA v2 -
Conceptual Captions

**OCR / Documents** - ICDAR - SynthText/MJSynth - FUNSD - DocVQA

**Medical** - ISIC - CheXpert - MIMIC-CXR - BraTS

**Remote Sensing** - DOTA - xView - SpaceNet - EuroSAT - BigEarthNet

------------------------------------------------------------------------

## Important access notes

-   **ImageNet:** the official site currently reports 14,197,122 indexed
    images and 21,841 synsets. The original image download requires
    login/request access; the ILSVRC 2012 subset contains 1,281,167
    training, 50,000 validation and 100,000 test images. [Official
    download](https://www.image-net.org/download.php)
-   **COCO:** use the official download page for images and annotations.
    [COCO downloads](https://cocodataset.org/#download)
-   **KITTI:** current downloads require registration and a stated
    purpose. The object benchmark provides separate image, LiDAR,
    calibration and label downloads. [KITTI
    registration](https://www.cvlibs.net/datasets/kitti/user_register.php)
-   **nuScenes:** the official dataset includes camera, LiDAR, radar,
    GPS/IMU and 3D annotations; the official download page provides the
    full and mini versions. [nuScenes
    download](https://www.nuscenes.org/download)
-   **ADE20K:** full dataset download requires registration/login and
    acceptance of its terms. [ADE20K](https://ade20k.csail.mit.edu/)
-   **Oxford-IIIT Pet / Flowers:** the VGG pages provide the dataset
    files and annotations; Pet is about 800 MB.
    [Pets](https://www.robots.ox.ac.uk/~vgg/data/pets/) ·
    [Flowers-102](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/)
-   **CIFAR:** the University of Toronto page provides the CIFAR-10 and
    CIFAR-100 archives directly. [CIFAR
    downloads](https://www.cs.toronto.edu/~kriz/cifar.html)

------------------------------------------------------------------------

## Suggested folder structure

``` text
computer-vision-datasets/
├── classification/
│   ├── MNIST/
│   ├── CIFAR10/
│   ├── CIFAR100/
│   └── ImageNet/
├── detection/
│   ├── VOC/
│   ├── COCO/
│   ├── OpenImages/
│   └── Objects365/
├── segmentation/
│   ├── Cityscapes/
│   ├── ADE20K/
│   └── COCO/
├── pose/
│   ├── COCO-Keypoints/
│   └── MPII/
├── video/
│   ├── UCF101/
│   ├── Kinetics/
│   └── SomethingSomethingV2/
├── autonomous-driving/
│   ├── KITTI/
│   ├── nuScenes/
│   ├── Waymo/
│   └── SemanticKITTI/
├── vision-language/
│   ├── COCO-Captions/
│   ├── VisualGenome/
│   └── VQA/
├── medical/
├── remote-sensing/
└── 3d/
```

### Sources

-   [COCO](https://cocodataset.org/)
-   [ImageNet](https://www.image-net.org/)
-   [KITTI](https://www.cvlibs.net/datasets/kitti/)
-   [nuScenes](https://www.nuscenes.org/)
-   [ADE20K](https://ade20k.csail.mit.edu/)
-   [Oxford VGG datasets](https://www.robots.ox.ac.uk/~vgg/data/)
-   [CIFAR](https://www.cs.toronto.edu/~kriz/cifar.html)
