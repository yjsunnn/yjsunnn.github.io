# Exploring the Role of Masking in Burst Image Super-Resolution 

<hr>
<i> In this paper, we explore the role of masking in facilitating the
learning of burst models. To our best knowledge, this is the first work diving deep
into the masking mechanism in low-level vision tasks, as major attention is paid
to masked image modeling in high-level visual representation learning. Empirical
investigations indicate that a proper masking mechanism applied to the common
pipeline of BurstSR can improve the alignment and fusion of the model, given
certain preconditions.


## Package dependencies
The project is built with PyTorch 1.10.1, Python3.9, CUDA10.1. For package dependencies, you can install them by:
```bash
pip3 install -r requirements.txt
```

## Pretrained model

- BaseModel(0.0) and MBM(0.5) [[Google Drive]](https://drive.google.com/drive/folders/1_8yGvHa4fo7qkZZ_1tBCzB4iDcEHG5T1?usp=share_link).


## Data preparation 
### Alignment
For training and testing data of Burst, first you should align the burst frames using homography_alignment.py
```python
python homography_alignment.py
```
The aligned frames could be put into '../LR_aligned' and then you should use the **aligned frames** as the input of the following training and testing.


## Evaluation
If you want to use your own data, the resolution of data should >=160x160, and the setting could be changed in ManualDataset.py and test_in_any_resolution.py.

For convenient evaluation, you could use data [[here]](https://drive.google.com/file/d/1I9WZCB8MGEc4MJe_WJXhx50AakbK15aL/view?usp=sharing) for evaluation.
It is worth noting that the data is not included in training or testing of our BaseModel and MBM.

### test for arbitrary resolution

```python
python homography_alignment.py
python test_in_any_resolution.py --arch BaseModel --weights ./checkpoints/0.0/model_best.pth --save_images
```

or

```python
python homography_alignment.py
python test_in_any_resolution.py --arch MBM --mask_ratio 0.5 --weights ./checkpoints/0.5/model_best.pth --save_images
```

## Training
### Base Model
To train BaseModel on RealBSR, we use 2 V100 GPUs and run for 400 epochs:

```python
python3 ./train.py --arch BaseModel --batch_size 16 --gpu '0,1' --train_ps 160 --env 64_0523_MotionMFSR_pixelmask0 --embed_dim 64 --warmup
```

To train MBM on RealBSR, we use 2 V100 GPUs and run for 400 epochs:

```python
python3 ./train.py --arch MBM --mask_ratio 0.5 --batch_size 16 --gpu '0,1' --train_ps 160 --env 64_0523_MotionMFSR_pixelmask5 --embed_dim 64 --warmup
```
