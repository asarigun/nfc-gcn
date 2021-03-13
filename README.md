# Graph Node-Feature Convolution for Representation Learning in TensorFlow


<p align="center">
  <a href="https://arxiv.org/abs/1812.00086"><img src="https://img.shields.io/badge/Paper-Report-red"/></a>
  <a href="https://github.com/LiZhang-github/NFC-GCN"><img src="https://img.shields.io/badge/Official-Code-ff69b4"/></a>
  <a href="https://github.com/asarigun/nfc-gcn/blob/main/LICENSE"><img src="https://img.shields.io/github/license/thudm/cogdl"/></a>
</p>


<p align="center"><img width="20%" src="https://github.com/asarigun/nfc-gcn/blob/main/images/tensorflow_logo.png"></p>

Implementation of Graph Node-Feature Convolution for Representation Learning in TensorFlow

![Graph Node-Feature Convolution for Representation Learning](https://github.com/asarigun/nfc-gcn/blob/main/images/figure.jpg)

Graph convolutional network (GCN) is an emerging neural network approach.  It learns new representation of a node by aggregating feature vectors of all neighbors in the aggregation process without considering whether the neighbors or features are useful or not. Recent methods have improved solutions by sampling a fixed size set of neighbors, or assigning different weights to different neighbors in the aggregation process, but features within a feature vector are still treated equally in the aggregation process. In this paper, a new convolution operation is introduced on regular size feature maps constructed from features of a fixed node bandwidth via sampling to get the first-level node representation, which is then passed to a standard GCN to learn the second-level node representation. Experiments show that the method out performs competing methods in semi-supervised node classification tasks. Furthermore, it is believed that this method opens new doors for exploring new GCN architectures, particularly deeper GCNmodels.

Li  Zhang , Heda Song, Haiping  Lu, 2018, https://arxiv.org/abs/1812.00086 

For official implementation  https://github.com/LiZhang-github/NFC-GCN


## Requirements
* tensorflow_version 1.x

## Training

```bash
python train.py
```

Note: Since random inits, your training results may not exact the same as reported in the paper!

You can specify a dataset as follows:

* For Citeseer: 
```bash
python train.py --dataset citeseer
```
* For Cora: 
```bash
python train.py --dataset cora
```
* For Pubmed: 
```bash
python train.py --dataset pubmed
```
(or by editing `train.py`)


## Reference

[1] [Zhang, Song, Lu, Graph Node-Feature Convolution for Representation Learning, 2018](https://arxiv.org/abs/1812.00086)  [![report](https://img.shields.io/badge/Official-Code-yellow)](https://github.com/LiZhang-github/NFC-GCN)

[2] [Kipf & Welling, Semi-Supervised Classification with Graph Convolutional Networks, 2016](https://arxiv.org/abs/1609.02907)  [![report](https://img.shields.io/badge/Official-Code-ff69b4)](https://github.com/tkipf/gcn)



