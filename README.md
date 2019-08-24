# S3D in PyTorch
S3D Network is reported in the ECCV 2018 paper [Rethinking Spatiotemporal Feature Learning: Speed-Accuracy Trade-offs in Video Classification](https://arxiv.org/abs/1712.04851). It has been shown by Xie that replacing standard 3D convolutions with spatial and temporal separable 3D convolutions 1) reduces the total number of parameters, 2) is more computationally efficient, and even 3) improves the performance in terms of accuracy.

## Overview
In this repository, we release the pretrained S3D network in PyTorch. We pretrained S3D on Kinetics-400 dataset and it achieves 72.08% top1 accuracy (top5: 90.35%) on the validation set of the dataset.

|         Network         |  Top 1 (%)  |  Top 5 (%) |
|:------------------:| :----:| :----:|
| I3D | 71.1 | 89.3 |
| S3D (reported by author) | 72.2 | 90.6 |
| S3D (our implementation) | 72.1 | 90.4 |

## Weight file & Sample code
First, clone this repository and download [this weight file](https://drive.google.com/uc?export=download&id=1HJVDBOQpnTMDVUM3SsXLy0HUkf_wryGO). Then, just run the code using

`$ python main.py`

This will output the top 5 Kinetics classes predicted by the model with corresponding probability.

![](sample.gif)

```
Top 5 classes ... with probability
riding a bike ... 0.88421476
riding scooter ... 0.05233049
motorcycling ... 0.029078288
riding unicycle ... 0.008401934
faceplanting ... 0.005443991
```

## Notes
We implement and release this repository together with our [TASED-Net project](https://github.com/kylemin/TASED-Net.git). If you find it useful, you might want to consider citing our work.

```
@article{min2019tased,
  title={TASED-Net: Temporally-Aggregating Spatial Encoder-Decoder Network for Video Saliency Detection},
  author={Min, Kyle and Corso, Jason J},
  journal={arXiv preprint arXiv:1908.05786},
  year={2019}
}
```
