# tensorflow-s530fn
TensorFlow 1.14.1 build for Asus VivoBook S15 (X530FN_S530FN). The whl file is created by following instructions found on https://www.tensorflow.org/install/source. 


To install:

```bash
pip install tensorflow-<version-tags>.whl
```


To test your TensorFlow installa: 
```bash
# GPU
python3 convolutional.py

# CPU
export CUDA_VISIBLE_DEVICES=""
python3 convolutional.py
```


#### Additional information

lshw output
```bash
sudo lshw | grep product
```
```
    product: VivoBook_ASUSLaptop X530FN_S530FN
       product: X530FN
             product: 8ATF1G64HZ-2G6E1
             product: 8ATF1G64HZ-2G6E1
          product: Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz
          product: Intel Corporation
             product: Intel Corporation
             product: Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Thermal Subsystem
             product: Xeon E3-1200 v5/v6 / E3-1500 v5 / 6th/7th Gen Core Processor Gaussian Mixture Model
             product: Intel Corporation
             product: Intel Corporation
                product: xHCI Host Controller
                   product: USB Optical Mouse
                   product: USB2.0 HD UVC WebCam
                product: xHCI Host Controller
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
                product: GP108M [GeForce MX150]
             product: Intel Corporation
             product: Intel Corporation
                product: Wireless 8265 / 8275
             product: Intel Corporation
                product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
             product: Intel Corporation
```

NVIDIA and CUDA versions 
```bash
nvidia-smi | grep Driver
```
```
| NVIDIA-SMI 430.26       Driver Version: 430.26       CUDA Version: 10.2     |
```

CUDNN version
```bash
cat /usr/include/cudnn.h | grep CUDNN_MAJOR -A 2
```
```
#define CUDNN_MAJOR 7
#define CUDNN_MINOR 6
#define CUDNN_PATCHLEVEL 2
--
#define CUDNN_VERSION (CUDNN_MAJOR * 1000 + CUDNN_MINOR * 100 + CUDNN_PATCHLEVEL)

#include "driver_types.h"
```

TensorRT version
```bash
dpkg -l | grep TensorRT
```
```
ii  graphsurgeon-tf                                             5.0.2-1+cuda10.0                                amd64        GraphSurgeon for TensorRT package
ii  libnvinfer-dev                                              5.0.2-1+cuda10.0                                amd64        TensorRT development libraries and headers
ii  libnvinfer-samples                                          5.0.2-1+cuda10.0                                all          TensorRT samples and documentation
ii  libnvinfer5                                                 5.0.2-1+cuda10.0                                amd64        TensorRT runtime libraries
ii  python3-libnvinfer                                          5.0.2-1+cuda10.0                                amd64        Python 3 bindings for TensorRT
ii  python3-libnvinfer-dev                                      5.0.2-1+cuda10.0                                amd64        Python 3 development package for TensorRT
ii  tensorrt                                                    5.0.2.6-1+cuda10.0                              amd64        Meta package of TensorRT
ii  uff-converter-tf                                            5.0.2-1+cuda10.0                                amd64        UFF converter for TensorRT package
```

Python version
```bash
python3 --version
```
```
Python 3.6.8
```
