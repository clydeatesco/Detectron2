# Detectron2
Detectron2 + Yolov7

```bash
> conda create -n yolov7_mask python=3.9
> conda activate yolov7_mask
> conda install pytorch==1.12.0 torchvision==0.13.0 torchaudio==0.12.0 cudatoolkit=11.6 -c pytorch -c conda-forge
> cd yolov7
> git clone https://github.com/facebookresearch/detectron2.git
> cd detectron2 && code .
# Navigate to https://github.com/WongKinYiu/yolov7/tree/mask and download as zip file
# directory structure yolov7/detectron2 and yolov7/yolov7-mask
> pip install -e .
# installation fix: macro set inside setup.py link here https://github.com/Ikomia-dev/detectron2/commit/cf546cfdae29b1f032f58a7d0340140443ee0603
> cd .. && cd yolov7-mask
# no need to install torch
```bash

```bash
line 11: # torch>=1.7.0,!=1.12.0
line 12: # torchvision>=0.8.1,!=0.13.0
```

```bash
>pip install -r requirements.txt

> python segment.py --source image1.jpg --nosave --view-img
# error: AttributeError: 'Upsample' object has no attribute 'recompute_scale_factor'
# fix: https://github.com/ultralytics/yolov5/issues/6948

> python segment.py --source clyde_sample1.jpg --nosave --view-img
> python segment.py --source clyde_sample1.jpg --nosave --view-img --nobbox
> python segment.py --source clyde_sample1.jpg --nosave --view-img --nobbox --nolabel
> python segment.py --source ac_parkour.mp4 --nosave --view-img --nobbox --nolabel --showfps
```
