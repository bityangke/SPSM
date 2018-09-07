This is the code for AAAI 2019 submission "Weakly Supervised Semantic Segmentation by Selecting High-quality Pixels and Masks"

License
SPSM is released under the MIT License (refer to the LICENSE file for details).

Training:
STEP 1:
The proposed mask selection strategy can boost the segmentation performance, especially for SPSM-Resnet101. We have release the selected annotations in 3 iterations for Resnet101 based models and the final annotations for VGG16 based model. 

You can download it from [Baidu Yun dataset](https://pan.baidu.com/s/1vYiNzcYmqqv08lb2Ub-n3Q) or [Google Driver dataset](https://drive.google.com/open?id=1wK9Utrvz1A6qCjeBWL_V9FS1U2ChwK3o)

STEP 2:
download the pascal voc 2012 dataset and change the DATA_DIRECTORY in the script according to your setting.

STEP 3:
Training model for SPSM-Resnet101:
You can try to train your own models using code main.py in https://github.com/zmbhou/Deeplab-v2--ResNet-101--Tensorflow/, and set the initial LR=4e-5 and the maxiter as 18000. The mIoU of three iterations are reported as 59.9, 61.3 and 61.3 without multi-scale fusion in our submission. Note that the training for each iteration is initialized by deeplab_resnet_init.ckpt.

Training model for SPSM-VGG16:
You can try to train your own models using code https://github.com/ankurgupta26/deepLabv2 for SPSM-VGG16, with LR=1e-4 and maxiter=18000 in (12). The mIoU is 56.9 without multi-scale fusion in our submission.


Testing:
Step 1: download the compressed model from [Baidu Yun model](https://pan.baidu.com/s/1NUyug2XuKS2vsWJgdFynkw) or [Google Driver model](https://drive.google.com/open?id=1jwKlEvBdbzzMJxL3BDAsjMvbUBBrlcPz)
and put it in the root folder and unzip it.

Step 2: Run test_vocspsm_vgg.py for SPSM-vgg16 evaluation, the predictions will be saved in SAVE_DIR = './result/'. Mean IoU of 58.4 can be achieved.

Step 3: Run test_vocspsm_resnet for SPSM-resnet101 evaluation, the predictions will be saved in SAVE_DIR = './result/'. Mean IoU of 61.6 can be achieved.

Step 4:  Please refer to Deeplabv2 for runing CRF as post-processing. The mean IoU of 59.9 and 62.3 can be achieved for SPSM-vgg16 and SPSM-resnet101, respectively. The released results on PASCAL VOC 2012 val and test datasets are contained in [Baidu Yun dataset](https://pan.baidu.com/s/1vYiNzcYmqqv08lb2Ub-n3Q) or [Google Driver dataset](https://drive.google.com/open?id=1wK9Utrvz1A6qCjeBWL_V9FS1U2ChwK3o)
