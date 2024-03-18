---
description: Authored 10/17/23
---

# Evaluating Linearity, Modulation Effects, and Experimental Challenges

### Key Points

* A linear response exists between 0-15mW when there's no modulation ([fig 1](evaluating-linearity-modulation-effects-and-experimental-challenges.md#figures)).
* Imaging in the absence of modulation introduces significant noise ([fig 2](evaluating-linearity-modulation-effects-and-experimental-challenges.md#figures)).
* Efforts to image the 605nm fluorophore have so far yielded no meaningful results.
* Enhancing ambient light control could improve data quality.
* To achieve successful imaging of the 605nm fluorophore, substituting the 90/10 splitter with a 45-degree mirror might be essential.

### Experimental Procedure

1. A diluted sample of the 625nm fluorophore was prepared and positioned on a pristine glass slide.
2. The slide was situated beneath the objective, ensuring a single fluorophore was distinctly in focus.
3. Using the image obtained from the CMOS camera and employing the full wave at half power method, the fluorophore's dimensions were gauged and found to be 4µm.
4. Adjustments were made to the excitation power, ranging from 0-20mW.
5. For each power increment, an EBIS output recording was made.
6. These recordings underwent analysis to deduce the linearity of the responses ([fig 1](evaluating-linearity-modulation-effects-and-experimental-challenges.md#figures)).
7. The complete recording at 10mW power was integrated into a singular spatial frame using 100ms timesteps ([fig 2](evaluating-linearity-modulation-effects-and-experimental-challenges.md#figures)).
8. This recording was subsequently converted into a 30fps movie, retaining a 100ms frame accumulation duration ([supplementary materials](evaluating-linearity-modulation-effects-and-experimental-challenges.md#supplementary-materials)).
9. Similar procedures were carried out for the 605nm fluorophore; however, the efforts did not yield discernible outcomes.

### Results

The data distinctly showcases a linear correlation between 0-15mW ([fig 1](evaluating-linearity-modulation-effects-and-experimental-challenges.md#figures)) for the 625nm fluorophore. Nevertheless, both the video and single-frame presentations exhibited noticeable noise, which poses a challenge for interpretation. Calibration efforts to concurrently minimize this noise while conserving the signal's integrity were hampered by erratic response fluctuations, both temporally and in intensity.

### Discussion

Our principal findings highlight the consistent linear response of the 625nm fluorophore within the 0-15mW range, establishing a foundation for future experimental predictability. However, the pervasive noise in the data raises concerns. This noise, particularly pronounced in non-modulated imaging, obscures signal clarity and introduces unpredictability in its temporal and intensity responses.

The inability to derive tangible results from the 605nm fluorophore stems primarily from a combination of fluorophore size, and the diminished response of the signal as it passes through the various filter stages. Because of this, it is essential that we preserve every photon possible when imaging the 605nm signal. It may be desirable to replace the 90/10 splitter with a flippable or otherwise removable mirror.

Noise's pronounced presence underscores the pressing need to control the light available to the sensor. Improved baffling of the camera system could result in improved imaging results especially when there is no periodicity to tune to.

In our future endeavors, it should be considered whether modulated or non-modulated setup is preferrable. In the modulated case the events of interest are easier to tune for, however, saturation of the 625nm fluorophore in particular becomes a concern. In the non-modulated case, noise is the primary challenge to be overcome. In either case, increasing the signal from the 605nm fluorophore is essential.

### Figures

1.

    <figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption><p>Events/Second/Power level</p></figcaption></figure>


2.

    <figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption><p>Unmodulated output from the EBIS (FOV: 100um)</p></figcaption></figure>



### Supplementary Materials

{% file src="../.gitbook/assets/625_fluorophore_unmodulated_30fps.avi" %}
Video of EBIS output for the 625nm fluorophore
{% endfile %}
