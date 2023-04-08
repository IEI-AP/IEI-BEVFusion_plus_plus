# IEI-BEVFusion++
This method is built based on the BEVFusion framework, which uses two separate branches that encoder camera and LiDAR inputs into a unified BEV space, and fuses these features for prediction. We first strengthen the LiDAR-based encoder by fusing the multi-level BEV features derived from different stages of the sparse convolution and increasing the channel number. To further exploit the information from the camera, we introduce an auxiliary prediction branch using only the BEV features from the camera encoder during training. Moreover, we employ the multi-modal GT-Paste algorithm to alleviate the class imbalance problem.
## Results
### 3D Object Detection (on nuScenes test)

|        Model         |  mAP  |  NDS  |
| :------------------: | :---: | :---: |
| IEI-BEVFusion++(TTA+Model ensemble) | 0.757 | 0.776 |

### 3D Object Detection (on nuScenes val)

|                      Model                      |  mAP  |  NDS  |
| :---------------------------------------------: | :---: | :---: |
| IEI-BEVFusion++(voxel size=0.075, BEV size=360) | 0.714 | 0.735 |

## Get Started

### Environment
This implementation is build upon [mmdetection3d](https://github.com/open-mmlab/mmdetection3d), please follow the steps in [install.md](./docs/install.md) to prepare the environment.

### Data
Please follow the official instructions of mmdetection3d to process the nuScenes dataset.(https://mmdetection3d.readthedocs.io/en/latest/advanced_guides/datasets/nuscenes_det.html)


## Acknowledgement
Many thanks to the following open-source projects:
* [mmdetection3d](https://github.com/open-mmlab/mmdetection3d)

## Reference

```bibtex
@{author={Gongzhan, Zhaoyun, Zhuhong}}
```
