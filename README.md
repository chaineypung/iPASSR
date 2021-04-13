# iPASSR
**PyTorch implementation of "*Symmetric Parallax Attention for Stereo Image Super-Resolution*", NTIRE workshop at CVPR 2021. [<a href="https://arxiv.org/pdf/2011.03802.pdf">pdf</a>], [<a href="https://wyqdatabase.s3-us-west-1.amazonaws.com/iPASSR_visual_comparison.mp4">demo video</a>].**<br><br>

## *Highlights:*
#### 1. *We develop a Siamese network equipped with a bi-directional PAM to super-resolve both left and right images.*
  <p align="center"> <img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/Network.png" width="100%"></p>
  
#### 2. *We propose an inline occlusion handling scheme to deduce occlusions from parallax attention maps.*
  <p align="center"><img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/OcclusionDeduce.png" width="40%"><img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/OcclusionMask.png" width="55%"></p>
  
#### 3. *We design several illuminance-robust losses to enhance stereo consistency.* [[demo video](https://wyqdatabase.s3-us-west-1.amazonaws.com/iPASSR_illuminance_change.mp4)]
  <p align="center"> <img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/ResLoss.png" width="100%"></p>
  
#### 4. *Our iPASSR significantly outperforms PASSRnet with a comparable model size.*
  <p align="center"> <img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/Quantitative.png" width="100%"></p>
  <p align="center"> <img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/2xSR.png" width="100%"></p>
  <p align="center"> <img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/4xSR.png" width="100%"></p>
  <p align="center"> <img src="https://raw.github.com/YingqianWang/iPASSR/master/Figs/RealSR.png" width="100%"></p>

## Download the Results
**We share the quantitative and qualitative results achieved by our iPASSR on all the test sets for both 2xSR and 4xSR. Then, researchers can compare their algorithms to our method without performing inference. Results are available at [Baidu Drive](https://pan.baidu.com/s/1w8RtQau2RoY89jsFvMCStw) (Key: NUDT).**
<br>

## Requirement
* **PyTorch 1.3.0, torchvision 0.4.1. The code is tested with python=3.7, cuda=9.0.**
* **Matlab (For training/test data generation and performance evaluation)**

## Train
* **Download the training sets from [Baidu Drive](https://pan.baidu.com/s/173UGmmN0rtOUghIT40oy8w) (Key: NUDT) and unzip them to `./data/train/`.** 
* **Run `./data/train/GenerateTrainingPatches.m` to generate training patches.**
* **Run `train.py` to perform training. Checkpoint will be saved to  `./log/`.**

## Test
* **Download the test sets and unzip them to `./data`. Here, we provide the full test sets used in our paper on [Baidu Drive](https://pan.baidu.com/s/1SIYGcMBEDDZ0wYrkxL9bnQ) (Key: NUDT).** 
* **Run `test.py` to perform a demo inference. Results (`.png` files) will be saved to `./results`.**
* **Run `evaluation.m` to calculate PSNR and SSIM scores.**

## Some Useful Recources
* **The 2x/4x models of EDSR/RDN/RCAN retrained on stereo image datasets. [Baidu Drive](https://pan.baidu.com/s/1GrKi8taYnEColKz_wa5f4w) (Key: NUDT).**
* **Original results of StereoSR.

## Citiation
**We hope this work can facilitate the future research in stereo image SR. If you find this work helpful, please consider citing:**
```
@article{iPASSR,
  author    = {Wang, Yingqian and Ying, Xinyi and Wang, Longguang and Yang, Jungang and An, Wei and Guo, Yulan},
  title     = {Symmetric Parallax Attention for Stereo Image Super-Resolution},
  journal   = {IEEE Conference on Computer Vision and Pattern Recognition Workshops (CVPRW)},
  year      = {2021},
}
```

## Contact
**Any question regarding this work can be addressed to [wangyingqian16@nudt.edu.cn](wangyingqian16@nudt.edu.cn) and [yingxinyi18@nudt.edu.cn](yingxinyi18@nudt.edu.cn).**
