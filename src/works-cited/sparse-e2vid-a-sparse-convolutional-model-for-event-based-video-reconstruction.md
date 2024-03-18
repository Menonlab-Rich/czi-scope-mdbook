---
description: >-
  https://openaccess.thecvf.com/content/CVPR2023W/EventVision/html/Cadena_Sparse-E2VID_A_Sparse_Convolutional_Model_for_Event-Based_Video_Reconstruction_Trained_CVPRW_2023_paper.html
---

# Sparse-E2VID: A Sparse Convolutional Model for Event-Based Video Reconstruction

Event cameras are image sensors inspired by biology and offer several advantages over traditional frame-based cameras. However, most algorithms for reconstructing images from event camera data do not exploit the sparsity of events, resulting in inefficient zero-filled data. Given that event cameras typically have a sparse index of 90% or higher, this is particularly wasteful. In this work, we propose a sparse model, Sparse-E2VID, that efficiently reconstructs event-based images, reducing inference time by 30%. Our model takes advantage of the sparsity of event data, making it more computationally efficient, and scales better at higher resolutions. Additionally, by using data augmentation and real noise from an event camera, our model reconstructs nearly noise-free images. In summary, our proposed model efficiently and accurately reconstructs images from event camera data by exploiting the sparsity of events. This has the potential to greatly improve the performance of event-based applications, particularly at higher resolutions. Some results can be seen in the following video: [https://youtu.be/sFH9zp6kuWE](https://youtu.be/sFH9zp6kuWE)
