
<p align="center">

  <h2 align="center">Animate-X: Universal Character Image Animation with Enhanced Motion Representation</h2>
  <p align="center">
    <a href=""><strong>Shuai Tan</strong></a>
    ·
    <a href="https://scholar.google.com/citations?user=BwdpTiQAAAAJ"><strong>Biao Gong</strong></a><sup>†</sup>
    ·
    <a href="https://scholar.google.com/citations?user=cQbXvkcAAAAJ"><strong>Xiang Wang</strong></a>
    ·
    <a href="https://scholar.google.com/citations?user=ZO3OQ-8AAAAJ"><strong>Shiwei Zhang</strong></a>
    <br>
    <a href="https://openreview.net/profile?id=~DanDan_Zheng1"><strong>Dandan Zheng</strong></a>
    ·
    <a href="https://scholar.google.com.hk/citations?user=S8FmqTUAAAAJ"><strong>Ruobing Zheng</strong></a>
    ·
    <a href="https://scholar.google.com/citations?user=hMDQifQAAAAJ"><strong>Kecheng Zheng</strong></a>
    ·
    <a href="https://openreview.net/profile?id=~Jingdong_Chen1"><strong>Jingdong Chen</strong></a>
    ·
    <a href="https://openreview.net/profile?id=~Ming_Yang2"><strong>Ming Yang</strong></a>            
    <br>
    <br>
        <a href="https://arxiv.org/abs/2410.10306"><img src='https://img.shields.io/badge/arXiv-Animate--X-red' alt='Paper PDF'></a>
        <a href='https://lucaria-academy.github.io/Animate-X/'><img src='https://img.shields.io/badge/Project_Page-Animate--X-blue' alt='Project Page'></a>
    <br>
    <b></a>Ant Group &nbsp; | &nbsp; </a>Tongyi Lab  </b>
    <br>
  </p>
</p>

This repository is the official implementation of paper "Animate-X: Universal Character Image Animation with Enhanced Motion Representation". Animate-X is a universal animation framework based on latent diffusion models for various character types (collectively named X), including anthropomorphic characters.
  <table align="center">
    <tr>
    <td>
      <img src="https://github.com/user-attachments/assets/fb2f4396-341f-4206-8d70-44d8b034f810">
    </td>
    </tr>
  </table>


## &#x1F4CC; Updates
* [2024.12.10] 🔥 We release our [Animate-X](https://github.com/antgroup/animate-x) codes and models.
* [2024.10.14] 🔥 Our [paper](https://arxiv.org/abs/2410.10306) is in public on arxiv.



<!-- <video controls loop src="https://cloud.video.taobao.com/vod/vs4L24EAm6IQ5zM3SbN5AyHCSqZIXwmuobrzqNztMRM.mp4" muted="false"></video> -->

## &#x1F304; Gallery
### Introduction 
<table class="center">
<tr>
    <td width=47% style="border: none">
        <video controls loop src="https://github.com/user-attachments/assets/085b70c4-cb68-4ac1-b45f-ed7f1c75bd5c" muted="false"></video>
    </td>
    <td width=53% style="border: none">
        <video controls loop src="https://github.com/user-attachments/assets/f6275c0d-fbca-43b4-b6d6-cf095723729e" muted="false"></video>
    </td>
</tr>
</table>

### Animations produced by Animate-X
<table class="center">
<tr>
    <td width=50% style="border: none">
        <video controls loop src="https://github.com/user-attachments/assets/732a3445-2054-4e7b-9c2d-9db21c39771e" muted="false"></video>
    </td>
        <td width=50% style="border: none">
        <video controls loop src="https://github.com/user-attachments/assets/f25af02c-e5be-4cab-ae64-c9e0b392643a" muted="false"></video>
    </td>
</tr>
</table>




## &#x1F680; Installation
Install with `conda`: 
```bash
conda env create -f environment.yaml
conda activate animate-x
```


## &#x1F680; Download Checkpoints
Download Animate-X [checkpoints](https://xxxx) and put all files in `model` dir, which should be like:
```
models/
  xxxx.pth
  xxxxx.pth
  xxxx.pth
```

## &#x1F4A1; Inference 

We offer two inference modes. (1) The **easy mode** requires an input of a driven image and a dance video. (2) The **advanced mode** allows for more precise pose customization and alignment. In this mode, users can upload a sequence of customized pose skeleton images to the model. In other words, in this mode, the model accepts three types of inputs: images, videos, and pose skeleton sequences, and produces a video as the output.

### Tutorial for easy mode
```bash
python xxxxx.py
```

### Tutorial for advanced mode *(with customized pose skeletons)*
```bash
python xxxxx.py
```

## &#x1F4E7; Acknowledgement
This repository is based on the following codebases:
* https://github.com/xxxxx
* https://github.com/xxxxx

## &#x1F4DA; Citation
If you find this codebase useful for your research, please use the following entry.
```BibTeX
@article{AnimateX2025,
  title={Animate-X: Universal Character Image Animation with Enhanced Motion Representation},
  author={Tan, Shuai and Gong, Biao and Wang, Xiang and Zhang, Shiwei and Zheng, Dandan and Zheng, Ruobing and Zheng, Kecheng and Chen, Jingdong and Yang, Ming},
  journal={arXiv preprint arXiv:2410.10306},
  year={2025}
}
```
