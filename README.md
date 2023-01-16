
# Source
PointCutMix - [paper](https://arxiv.org/abs/2101.01461.pdf)  

# Running Instructions

## Instalation
```
pip install -r requirements.txt
```
Torch needs installed according to the CUDA version - [torch](https://pytorch.org/get-started/locally/)  

## Compile EMD module
Because the module is based on cpp it needs to be compiled. To do this - 
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





