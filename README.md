# ST-cGAN
The codes for the work ""
## Quick Start
1. Create Environment
```bash
conda create -n <environment_name> python=3.8
conda activate <enviroment_name>
pip install -r requirements.txt
```
2. Download dataset as mentioned in [Data](#data) section
3. Run inference on pretrained weights
````buildoutcfg
python inference.py --dataroot=<DATASET> --model=<MODEL> --dataset_mode=<DATALOADER> 
````
## Training
```buildoutcfg
python train_test.py --dataroot=<DATASET> --model=<MODEL> --dataset_mode=<DATALOADER> 
```
For Tensorboard:
``tensorboard --logdir logs/
``

## Data
[QLIPP](https://www.ebi.ac.uk/biostudies/BioImages/studies/S-BIAD25?query=S-BIAD25#) can be downloaded from repo.
- The directory structure of the whole project is as follows:
```bash
.
├── Network
│   ├──datasets
│   │       └── dataset_*.py
│   ├──train.py
│   ├──test.py
│   └──...
├── model
│   └── TU_Synapse128
│       └── res_True_head_4_ch_512_nuclei
│           ├── UTransform-129.pth
│           └── *.pth
└── data
    └──Synapse
        ├── train
        │   ├── im_c001_z011_t000_p005_r0-256_c0-256_sl0-3.npy
        │   └── *.npy
        └── train_label
            ├── im_c000_z011_t000_p005_r0-256_c0-256_sl0-3.npy
            └── *.npy
```
---

## References
- [TransUNet](https://github.com/Beckschen/TransUNet)
- [TransFuse](https://github.com/Rayicer/TransFuse)
- [Road Extraction Using PyTorch](https://github.com/jeffwen/road_building_extraction)
- [Deep Residual-Unet](https://arxiv.org/pdf/1711.10684.pdf)
- [Squeeze-and-Excitation Networks](https://arxiv.org/pdf/1709.01507.pdf)
- [ResUNet++](https://arxiv.org/pdf/1911.07067.pdf)
- [Unet](https://arxiv.org/pdf/1505.04597.pdf)
- [Brain tumor segmentation](https://github.com/galprz/brain-tumor-segmentation)
- [pix2pix](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix)
