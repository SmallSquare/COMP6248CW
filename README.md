# Introduction

This repository is for the group course work of COMP6248.

# Environment

Requirement:
> Python >= 3.7.2
>
>pytorch >= 1.11
>
>matplotlib >= 3.3
>
>scipy >= 1.6

Conda virtual environment command example:

```
conda create -n [your_venv_name] python=3.7.2
conda install pytorch==1.11 torchvision torchaudio cudatoolkit=11.3 -c pytorch
conda install matplotlib scipy
```

# Plan

The aim is to reproduce the code of the
paper [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://openreview.net/forum?id=YicbFdNTTy)
.

First meeting: 10-April. The paper should have been read before the meeting.

Notice that the hand-in deadline is 13-May-2022 16:00.

## Experiments

### Information of datasets used in paper

| dataset              | size       | number of images | number of classes | Resolution   |
|----------------------|------------|-----------------:|------------------:|--------------|
| JFT-300M             | Unreleased |      303,000,000 |            18,291 | Unknown      |
| ImageNet 21k         | Unknown    |       14,197,122 |            21,841 | 469*387(avg) |
| ImageNet ILSVRC-2012 | 155GB      |        1,281,167 |             1,000 | 469*387(avg) |
| ImageNet ReaL (val)  | 6GB        |           50,000 |             1,000 | 469*387(avg) |
| CIFAR-10             | 170MB      |           60,000 |                10 | 32*32        |
| CIFAR-100            | 170MB      |           60,000 |               100 | 32*32        |
| Oxford Flowers-102   | 330MB      |            8,189 |               102 | around 500   |
| Oxford IIIT-Pets     | 775MB      |            7,394 |                37 | around 500   |

### Selection of experiments

Here are most of the experiments in the paper. We will reproduce some experiments with check marks.

* Build a standard ViT. √
* Pretrained ViT on JFT and finetune on other datasets comparing with other models like ResNet.
  ![1](img/1.png)
* Pretraining on different size of datasets of ImageNet, ImageNet-21k, and JFT- 300M.
* Training on random subsets of 9M, 30M, and 90M as well as the full JFT- 300M dataset.
  ![2](img/2.png)
* Transfer accuracy with increasing pre-training compute.
  ![3](img/3.png)
* Research into embedding filters.
* Research into positional embedding.
* Research into attention distance.
  ![4](img/4.png)
* The performance of ViT with self-supervision.
* Compare SGD and Adam on ResNet.
  ![5](img/5.png)
* Test different Transformer shapes.
  ![6](img/6.png)
* Compare positional embeddings of 1-D, 2-D and relative one.
  ![7](img/7.png)
* More research on axial attentions.
  ![8](img/8.png)
* Attention maps.
  ![9](img/9.png)

