---
layout: post
title: Image Inpainting
github: "https://github.com/hlm01/image_inpainting"
image: "/img/in-project/inpaint.png"
tech:
  - name: "Pytorch"
    icon: "/img/tech/pytorch.png"
  - name: "Python"
    icon: "/img/tech/python.png"
description: Implement Partial Convolution for free form impainitng
tags:
    - "AI/ML"
    - Research 
---

This project implements the free form image inpainting method proposed by Liu
et al. [2018] which utilizes partial convolutions to allow handling images with
irregular hole shapes. A U-Net architecture with convolutional layers replaced by
partial convolutions is used. Partial convolutions are masking-aware and renormalize the standard convolution to skip over hole regions. The method is evaluated on
the Flickr Faces HQ dataset of human face images. While some remaining artifacts
are present likely due to insufficient training, the results demonstrate the potential
of masking-aware partial convolutions for robust free-form image inpainting that
can better preserve image semantics compared to patch-based methods.