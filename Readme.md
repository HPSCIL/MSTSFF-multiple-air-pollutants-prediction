# MSTSFFN 

### A multiscale spatial-temporal-spectral feature fusion network for predicting multiple air pollutants ###

<font face="Times new roman" size=4>
This repo is the implementation of our manuscript entitled A multiscale spatial-temporal-spectral feature fusion network for predicting multiple air pollutants. The code is based on Pytorch 1.12.1, and tested on a GeForce RTX 4090 GPU with 24GB memory.


Accurate prediction of air quality at urban monitoring stations, while accounting for the complex interactions and impacts among multiple pollutants, is crucial for enhancing urban environmental quality and public health. However, current research predominantly focuses on predicting individual pollutant indicators, without incorporating the interactions between pollutants into the modeling process, leading to limitations in prediction accuracy and capability. To address this issue, a Multiscale Spatial-Temporal-Spectral Feature Fusion Network (MSTSFFN) for predicting multiple air pollutants at air quality monitoring stations is proposed. Experimental results on three urban air quality datasets showed that the proposed MSTSFFN outperformed the state-of-the-art methods in prediction various pollutants. MSTSFFN's structural framework and key modules for characterizing and fusing the multiscale features in temporal, spatial and spectral dimensions can also serve as the fundamental components of more general modeling structures for other multi-variant spatio-temporal dynamics. 

## Framework

![MSTSFFN](./Fig/MSTSFFN.png)


## Requirements
MSTSFF uses the following dependencies
 
- Pytorch 1.12.1 and its dependencies
- Numpy and Pandas
- CUDA 11.8 or latest version

## Folder Structure
We list the code of the major modules as follows:<br>
- The main function to train/test our model: [click here](./MSTSFFN/MODEL/main.py)<br>
- The source code of our model: [click here](./MSTSFFN/MODEL/model.py)<br>
- Train and test data preporcessing are located at: [click here](./MSTSFFN/MODEL/data_preprocess.py)<br>
- Metric computations: [click here](./MSTSFFN/MODEL/utils.py)<br>

## Arguments
We introduce some major arguments of our main function here.

Training settings:
- train\_rate: rate of train set<br>
- test\_rate: rate pf test set<br>
- lag: time length of hidtorical steps<br>
- pre\_len: time length of future steps<br>
- num\_nodes: the number of stations<br>
- batch\_size: training or testing batch size<br>
- input\_dim: the feature dimension of inputs<br> 
- learning\_rate: the learning rate at the beginning<br>
- epochs: training epochs<br>
- early\_stop_patience: the patience of early stopping<br>
- device: using which GPU to train our model<br>
- seed: the random seed for experiments<br>

Model hyperparameters:<br>
- d\_model: position encoding embedding dimension<br>
- n\_heads: the number of multi-head attention<br>
- d\_k: feature dimensions of each head in multi-head attention<br>
- cheb\_k: chebyshev polynomials order<br>
- hid_dim: hidden layer dimension of Chebyshev graph convolution<br>
- dropout: dropout rate<br>


## Citation
To Cite MSTSFFN in Publications<br>
- A paper describing MSTSFFN will be submitted to a scientific journal for publication soon<br>
- For now, you may just cite the URL of the source codes of MSTSFFN (https://github.com/HPSCIL/MSTSFF-multiple-air-pollutants-prediction) in your publications</font>
