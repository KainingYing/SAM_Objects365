# SAM-Objects365

## TODO
- [x] Release the download links.
- [ ] Release the toturial.

## Introduction

The goal of this project is to use [SAM](https://github.com/facebookresearch/segment-anything) to annotate masks on the basis of carefully annotated target detection datasets [Objects365](http://www.objects365.org/overview.html), thereby facilitating large-scale pre-training of general instance segmentation. The specific process is shown in the figure below

## Visualizations
We provide some annotations of our SAM-Objects365. More visualizations please refer to [this link](https://github.com/KainingYing/SAM_Objects365/releases/download/demo/obj365_500.zip).

<table>
  <tr>
    <td><img src="assets/objects365_v1_00319323.jpg" width="400" /></td> 
    <td><img src="assets/objects365_v1_00418898.jpg" width="400" /></td>
  </tr>
  <tr>
    <td><img src="assets/objects365_v1_00456796.jpg" width="400" /></td>
    <td><img src="assets/objects365_v2_00900358.jpg" width="400" /></td>
  </tr>
</table>

## How to use SAM-Objects365 ?

### Download
Firstly, you should download the Objects365 v2 by running following:
```shell
python download_dataset.py \
    --dataset-name objects365v2 \
    --save-dir ${SAVING PATH} \
    --unzip \
    --delete  # Optional, delete the download zip file
``` 

Next you need download following mask annotations:

**BaiduNetDisk**: https://pan.baidu.com/s/1KLncoQ9u7-ABrgyBKCwxGg (1234)

**OneDrive**: https://1drv.ms/f/s!AqU-46ABHrbCgc8bS9HfrrYjthzf0Q?e=6CHGjs

This dataset folder sholud be like:

```
objects365_v2
├── annotations
│   ├── sam_obj365_train_1700k.json
│   ├── sam_obj365_train_75k.json
│   ├── sam_obj365_val_5k.json
│   ├── zhiyuan_objv2_train.json
│   └── zhiyuan_objv2_val.json
├── sam_mask_json
│   ├── sam_obj365_train_1742k
│   ├── sam_obj365_train_75k
├── train
└── val
```

## Acknowledgement

We would like to express our heartfelt thanks for the following projects:

- [Segment Anything](https://github.com/facebookresearch/segment-anything)
- [Objects365](http://www.objects365.org/overview.html)
