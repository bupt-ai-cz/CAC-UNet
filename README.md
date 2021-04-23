# Multi-level-colonoscopy-malignant-tissue-detection-with-adversarial-CAC-UNet
Implementation detail for our paper ["Multi-level colonoscopy malignant tissue detection with adversarial CAC-UNet"](https://arxiv.org/pdf/2006.15954.pdf)

DigestPath 2019

The proposed scheme in this paper achieves the best results in MICCAI DigestPath2019 challenge (https://digestpath2019.grand-challenge.org/Home/) on colonoscopy tissue segmentation and classification task.

## Citation
Please cite this paper in your publications if it helps your research:

```
@article{zhu2020multi,
  title={Multi-level colonoscopy malignant tissue detection with adversarial CAC-UNet},
  author={Zhu, Chuang and Mei, Ke and Peng, Ting and Luo, Yihao and Liu, Jun and Wang, Ying and Jin, Mulan},
  journal={arXiv preprint arXiv:2006.15954},
  year={2020}
}
```

## Dataset
Description of dataset can be found here:
https://digestpath2019.grand-challenge.org/Dataset/

To download the the DigestPath2019 dataset, please sign the DATABASE USE AGREEMENT first at here:
https://digestpath2019.grand-challenge.org/Download/

If you have problems about downing the dataset, please contact us.

Image sample:
![](https://github.com/PkuMaplee/Multi-level-colonoscopy-malignant-tissue-detection-with-adversarial-CAC-UNet/blob/master/sample-image.jpg)

## Envs
- Pytorch 1.0
- Python 3+
- cuda 9.0+

install
```
$ pip install -r  requirements.txt
```

`apex` :  Tools for easy mixed precision and distributed training in Pytorch
```
$ git clone https://github.com/NVIDIA/apex
$ cd apex
$ pip install -v --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" ./
```

## Dataset
```
├── data/
│   ├── tissue-train-neg/     
│   ├── tissue-train-pos-v1/
```
## Preprocessing
```
$ cd code/
$ python preprocessing.py
```

## Training
```
$ cd code/
$ python train.py --config_file='config/cac-unet-r50.yaml'
```

