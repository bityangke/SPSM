This is the demo code for AAAI 2019 submission "Weakly Supervised Semantic Segmentation by Selecting High-quality Pixels and Masks"

License
SPSM is released under the MIT License (refer to the LICENSE file for details).
Training:
we have release the final annotations of VGG and Resnet101 based models. 

You can download it from https://pan.baidu.com/s/1TF2lAFnWzMF69wyX_P6Gpw

You can try to train your own models using code https://github.com/zmbhou/Deeplab-v2--ResNet-101--Tensorflow/ for SPSM-Resnet101.

You can try to train your own models using code https://github.com/ankurgupta26/deepLabv2 for SPSM-VGG16

Testing:
Step 1: download the compressed model from https://pan.baidu.com/s/1ZdOHDDLiVtZUZU6_LcSDUQ
and put it in the root folder and unzip it.

Step 2: Run test_vocspsm_vgg.py for SPSM-vgg16 evaluation, mean IoU of 58.4 can be achieved.

Step 3: Run test_vocspsm_resnet for SPSM-resnet101 evaluation, mean IoU of 61.3 can be achieved.

Step 4:  Please refer to Deeplabv2 for runing CRF as post-processing. The mean IoU of 59.9 and 62.2 can be achieved for SPSM-vgg16 and SPSM-resnet101, respectively.
