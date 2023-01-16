
# Source
PointCutMix - [paper](https://arxiv.org/abs/2101.01461.pdf)  

# Running Instructions

## Installation
```
pip install -r requirements.txt
```
Torch needs to be installed according to the CUDA version - [torch](https://pytorch.org/get-started/locally/)  

## Compile EMD module
The Earth-Mover's Distance module is based on cpp and needs to be compiled. To do this - 
```
cd emd
python3 setup.py install
```

## Data
Download alignment **ModelNet** [here](https://shapenet.cs.stanford.edu/media/modelnet40_normal_resampled.zip) and save in `modelnet40_normal_resampled`.  
Save under the top directory tau_PointCutMix or update the DATA_PATH variable in train_pointcutmix_k.py.

## Train
The default parameters are set to run point-transformer (the model we analyze) with the appropriate setting.  
```
CUDA_VISIBLE_DEVICES=0,1 python train_pointcutmix_k.py
```
Test accuracies are calculated during training.




