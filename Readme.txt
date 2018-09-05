This is the demo code for AAAI 2019 submission "Weakly Supervised Semantic Segmentation by Selecting High-quality Pixels and Masks"

License
SPSM is released under the MIT License (refer to the LICENSE file for details).

Training:
The proposed mask selection strategy can boost the segmentation performance, especially for SPSM-Resnet101. We have release the selected annotations in 3 iterations for Resnet101 based models and the final annotations for VGG16 based model. 

You can download it from https://pan.baidu.com/s/1vYiNzcYmqqv08lb2Ub-n3Q

Training model for SPSM-Resnet101:
You can try to train your own models using code main.py in https://github.com/zmbhou/Deeplab-v2--ResNet-101--Tensorflow/, and set the initial LR=4e-5 and the maxiter as 18000. The mIoU of three iterations are reported as 59.9, 61.3 and 61.3 without multi-scale fusion in our submission. Note that the training for each iteration is initialized by deeplab_resnet_init.ckpt.

Training model for SPSM-VGG16:
You can try to train your own models using code https://github.com/ankurgupta26/deepLabv2 for SPSM-VGG16, with LR=1e-4 and maxiter=18000 in (12). The mIoU is 56.9 without multi-scale fusion in our submission.


Testing:
Step 1: download the compressed model from https://pan.baidu.com/s/1NUyug2XuKS2vsWJgdFynkw
and put it in the root folder and unzip it.

Step 2: Run test_vocspsm_vgg.py for SPSM-vgg16 evaluation, mean IoU of 58.4 can be achieved.

Step 3: Run test_vocspsm_resnet for SPSM-resnet101 evaluation, mean IoU of 61.6 can be achieved.

Step 4:  Please refer to Deeplabv2 for runing CRF as post-processing. The mean IoU of 59.9 and 62.3 can be achieved for SPSM-vgg16 and SPSM-resnet101, respectively. The released results on PASCAL VOC 2012 val and test datasets are contained in https://pan.baidu.com/s/1vYiNzcYmqqv08lb2Ub-n3Q.
