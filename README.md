[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/prototypical-cross-attention-networks-for/multi-object-tracking-and-segmentation-on-2)](https://paperswithcode.com/sota/multi-object-tracking-and-segmentation-on-2?p=prototypical-cross-attention-networks-for)
# Prototypical Cross-Attention Networks for Multiple Object Tracking and Segmentation

This is the offical implementation of paper [PCAN](https://papers.nips.cc/paper/2021/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf) for MOTS. 

We also present a [trailer](https://www.youtube.com/watch?v=hhAC2H0fmP8) that consists of method illustrations and tracking & segmentation visualizations. Our project website contains more information: [vis.xyz/pub/pcan](https://www.vis.xyz/pub/pcan/).

> [**Prototypical Cross-Attention Networks for Multiple Object Tracking and Segmentation**](https://papers.nips.cc/paper/2021/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf)  
> **NeurIPS 2021, Spotlight**  
> Lei Ke, Xia Li, Martin Danelljan, Yu-Wing Tai, Chi-Keung Tang, Fisher Yu


<div align="center">
<img src="./figures/pcan_banner_new.gif" width="100%" />
</div>


## Abstract

Multiple object tracking and segmentation requires detecting, tracking, and segmenting objects belonging to a set of given classes. Most approaches only exploit the temporal dimension to address the association problem, while relying on single frame predictions for the segmentation mask itself. We propose Prototypical Cross-Attention Network (PCAN), capable of leveraging rich spatio-temporal information for online multiple object tracking and segmentation. PCAN first distills a space-time memory into a set of prototypes and then employs cross-attention to retrieve rich information from the past frames. To segment each object, PCAN adopts a prototypical appearance module to learn a set of contrastive foreground and background prototypes, which are then propagated over time. Extensive experiments demonstrate that PCAN outperforms current video instance tracking and segmentation competition winners on both Youtube-VIS and BDD100K datasets, and shows efficacy to both one-stage and two-stage segmentation frameworks. 

## Prototypical Cross-Attention Networks (PCAN)
<img src="figures/pcan-banner-final.png" width="800">

## Main results
#### Results on [BDD100K Benchmark](https://eval.ai/web/challenges/challenge-page/1295/leaderboard/3268)

| Detector  | mMOTSA-val | mIDF1-val | ID Sw.-val |                                            Scores-val                                            | mMOTSA-test | mIDF1-test | ID Sw.-test |                                            Scores-test                                            |                                             Config                                             |                                                                                        Weights                                                                                         |                                           Preds                                           |                                            Visuals                                            |
| :-------: | :--------: | :-------: | :--------: | :----------------------------------------------------------------------------------------------: | :---------: | :--------: | :---------: | :-----------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------: |
| ResNet-50 |    28.1    |   45.4    |    874     | [scores](https://dl.cv.ethz.ch/bdd100k/mots/scores-val/pcan-frcnn_r50_fpn_12e_mots_bdd100k.json) |    31.9     |    50.4    |     845     | [scores](https://dl.cv.ethz.ch/bdd100k/mots/scores-test/pcan-frcnn_r50_fpn_12e_mots_bdd100k.json) | [config](https://github.com/SysCV/pcan/blob/main/configs/segtrack-frcnn_r50_fpn_12e_bdd10k.py) | [model](https://hkustconnect-my.sharepoint.com/:u:/g/personal/lkeab_connect_ust_hk/EVdSxsVuKlFDg5I77VsFr4UB_KJQY4Dd_5ZUMJ6gG9A2Hw?e=IhqrfY) \| [MD5](https://dl.cv.ethz.ch/bdd100k/mots/models/pcan-frcnn_r50_fpn_12e_mots_bdd100k.md5) | [preds](https://dl.cv.ethz.ch/bdd100k/mots/preds/pcan-frcnn_r50_fpn_12e_mots_bdd100k.zip) | [visuals](https://dl.cv.ethz.ch/bdd100k/mots/visuals/pcan-frcnn_r50_fpn_12e_mots_bdd100k.zip) |

## Installation
Please refer to [INSTALL.md](docs/INSTALL.md) for installation instructions.

## Usages
Please refer to [GET_STARTED.md](docs/GET_STARTED.md) for dataset preparation and detailed running (training, testing, visualization, etc.) instructions.


## Related links
[Youtube Video](https://www.youtube.com/watch?v=hhAC2H0fmP8) | [Bilibili Video](https://www.bilibili.com/video/BV1Rb4y1i7zS?spm_id_from=333.999.0.0)|
[Zhihu Reading](https://zhuanlan.zhihu.com/p/445457150)

## Citation
If you find PCAN useful in your research or refer to the provided baseline results, please star :star: this repository and consider citing :pencil::
```
@inproceedings{pcan,
    author    = {Ke, Lei and Li, Xia and Danelljan, Martin and Tai, Yu-Wing and Tang, Chi-Keung and Yu, Fisher},
    booktitle = {Advances in Neural Information Processing Systems (NeurIPS)},
    title     = {Prototypical Cross-Attention Networks for Multiple Object Tracking and Segmentation},
    year      = {2021}
}
