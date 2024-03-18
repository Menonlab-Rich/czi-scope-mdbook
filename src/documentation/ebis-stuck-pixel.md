---
description: Published 10/04/2023
---

# EBIS Stuck Pixel

### Highlights

* Experiments suggest the existence of a stuck pixel on the Prophesee EVK3 EBIS
* Going forward, this will be mitigated by thresholding integrated images to a upper bound of mean + $$20\sigma$$

### Explanation

In a recent [experiment](../reports/updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md#addendums), spatiotemporal events recorded during the session were integrated to produce a visual representation. However, the resultant image exhibited an unexpectedly subdued intensity contrast (refer to [Fig. 1](ebis-stuck-pixel.md#figures)). A thorough investigation into the cause of this anomaly revealed that the normalization of pixel values within the range \[0, 1] played a significant role. Specifically, the presence of anomalously large values within the dataset acted as outliers, thereby dictating the normalization scale and consequently compressing the range of the majority of other pixel values.

A remedial measure was devised, involving the clipping of pixel values to a predetermined threshold. This threshold is determined based on the dataset's statistical properties, specifically the mean and standard deviation. It was observed that to produce the image from the original experiment, the image in [Fig. 1](ebis-stuck-pixel.md#figures), the clipping threshold needed to be set at \[mean + <200$$\sigma$$]. An unusually high value for $$\sigma$$ suggested the existence of stuck pixels in the sensor, which generate aberrantly high readings.

Subsequent experiments, where the data was clipped to \[mean + 20$$\sigma$$] produced images that were more representative of the actual event distribution (as shown in [Fig. 2](ebis-stuck-pixel.md#figures)). For the sake of consistency and accuracy, it has been decided that, unless otherwise specified, all individual frames in future experiments will be clipped at the upper end to a value of \[mean + 20$$\sigma$$].\


### Figures

1. ![](<../.gitbook/assets/image (12).png>)
2. ![](<../.gitbook/assets/image (33).png>)
