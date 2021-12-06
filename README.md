# HiNet: Deep Image Hiding by Invertible Network
This repo is the official code for

* [**HiNet: Deep Image Hiding by Invertible Network.**](https://openaccess.thecvf.com/content/ICCV2021/html/Jing_HiNet_Deep_Image_Hiding_by_Invertible_Network_ICCV_2021_paper.html) 
  * [*Junpeng Jing*](https://tomtomtommi.github.io/), [*Xin Deng*](http://www.commsp.ee.ic.ac.uk/~xindeng/), [*Mai Xu*](http://shi.buaa.edu.cn/MaiXu/zh_CN/index.htm), [*Jianyi Wang*](http://buaamc2.net/html/Members/jianyiwang.html), [*Zhenyu Guan*](http://cst.buaa.edu.cn/info/1071/2542.htm).

Published on [**ICCV 2021**](http://iccv2021.thecvf.com/home).
By [MC2 Lab](http://buaamc2.net/) @ [Beihang University](http://ev.buaa.edu.cn/).

![framework](./HiNet.png)

## Dependencies and Installation
- Python 3 (Recommend to use [Anaconda](https://www.anaconda.com/download/#linux)).
- [PyTorch = 1.0.1](https://pytorch.org/) .
- See [environment.yml](https://github.com/TomTomTommi/HiNet/blob/main/environment.yml) for other dependencies.


## Get Started
- Run `python train.py` for training.

- Run `python test.py` for testing.

- Set the model path (where the trained model saved) and the image path (where the image saved during testing) to your local path. 

    `line45:  MODEL_PATH = '' ` 

    `line49:  IMAGE_PATH = '' ` 

## Dataset
- In this paper, we use the commonly used dataset DIV2K, COCO, and ImageNet.

- For train or test on your own dataset, change the code in `config.py`:

    `line30:  TRAIN_PATH = '' ` 

    `line31:  VAL_PATH = '' `


## Trained model
- Here we provide a trained [model](https://drive.google.com/drive/folders/1l3XBFYPMaNFdvCWyOHfB2qIPkpjIxZgE?usp=sharing).

- Fill in the `MODEL_PATH` and the file name `suffix` before testing by the trained model.

- For example, if the model name is `model.pt` and its path is `/home/usrname/Hinet/model/`, 
set `MODEL_PATH = '/home/usrname/Hinet/model/'` and file name `suffix = 'model.pt'`.

## Others
- The `batchsize_val` in `config.py` should be at least `2*number of gpus` and it should be divisible by number of gpus.

## Citation
If you find our paper or code useful for your research, please cite:
```
@InProceedings{Jing_2021_ICCV,
    author    = {Jing, Junpeng and Deng, Xin and Xu, Mai and Wang, Jianyi and Guan, Zhenyu},
    title     = {HiNet: Deep Image Hiding by Invertible Network},
    booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)},
    month     = {October},
    year      = {2021},
    pages     = {4733-4742}
}

```
