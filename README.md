# FOAD-MFFF
ICIP2023--Flow-based one-class anomaly detection with Multi-frequency Feature fusion. International Conference on Image Processing. 
Accepted.


## Paper Introduction
Anomaly detection in computer vision seeks to identify samples outside of a predefined distribution, including texture defect detection and semantic anomaly detection. However,
existing methods are difficult to simultaneously achieve high performance for both types of anomaly detection. To address this issue, we propose a new flow-based anomaly detection
method. Firstly, we use semantic features extracted from a pre-trained backbone to learn the distribution of normal data from a semantic perspective. Secondly, we introduce a
multi-frequency feature fusion module to aggregate semantic and texture information, which substantially improves performance for both types of anomaly detection at the same
time. Extensive experiments on multiple well-known datasets demonstrate that our proposed method performs well in both types of anomaly detection, specially, achieves state-of-theart performance in one-class anomaly detection . The codes will be available at https://github.com/SYLan2019/FOADMFFF


## Installation

1. First clone the repository
   ```
   git clone https://github.com/SYLan2019/FOAD-MFFF.git
   ```
2. Create the virtual environment via conda
    ```
    conda create -n SANF-AD python=3.8
    ```
3. Activate the virtual environment.
    ```
    conda activate SANF-AD
    ```
4. Install the dependencies.
   ```
   pip install --user --requirement requirements.txt
   ```
   
## Configure and Run
All configurations concerning data, model, training etc, can be found in _config.py_. The default configuration will run a training with paper-given parameters on the Cifar10 dataset.

To replicate the results in the paper for CIFAR10  dataset, please set the paramater pretrained = False in _config.py_ and run the following commands to extract features:

``` shell
# CIFAR
python extractor.py
```

## Training
Then run the following code to train the model on the features of Cifar10
```
python train.py -h
```

### Training on CIFAR10
To train the model on CIFAR10 dataset for a given anomaly class, run the following:
``` 
python main.py 
```

