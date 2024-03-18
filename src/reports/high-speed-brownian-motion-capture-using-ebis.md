---
description: Authored 11/4/23
---

# High Speed Brownian Motion Capture using EBIS

### Key Points

* High-speed imaging of fluorophores at 10,000 FPS is possible.
* Brownian motion imaging was conducted using a 625nm fluorophore in a CoverWell™ Imaging Chamber.
* Imaging was enhanced by a haptic motor to improve light spread and add detectable motion.
* Clearer motion capture was achieved with motor-enhanced light modulation.
* Over accumulation technique used for sampling provided negligible returns at the cost of real-time video and increased noise.
* Very little motion was detected notwithstanding the strong signal.
* Future experiments could employ optimization methods like the Taguchi method to improve SNR without modulation, as well as improved methods for containing the fluorophores to allow for more motion.

### Experimental Setup

1. A dilute sample of 625nm fluorophore was prepared and placed into a[ CoverWell™ Imaging Chamber Gasket](https://www.thermofisher.com/order/catalog/product/C24727).
2. A glass sheet was carefully placed over the well to avoid compressing the sample, which allowed for the free movement of the fluorophores.
3. The sample was positioned under the objective lens for imaging.
4. A single fluorophore was brought into focus without the aid of the CMOS camera due to the CMOS suffering from focus drift, presumably from motion of the fluoropores.
5. Data for the fluorescent bead was recorded with a haptic motor attached to the fiber optic, enhancing the light spread and introducing light modulation.
6. Additional data was recorded with the motor turned off for comparison purposes.
7. The captured data was converted to video at a frame rate of 10,000 FPS, with the integration time set to equal the frame rate period See[ Supplemental materials 1](high-speed-brownian-motion-capture-using-ebis.md#supplemental-materials).
8. Individual frames were collected at a frame rate of 10,000 FPS with an integration time of 10ms, utilizing over accumulation ([Figure 4](high-speed-brownian-motion-capture-using-ebis.md#figures)).
9. The resulting videos and frame data were analyzed to assess motion clarity and SNR.

### Results

The experiment successfully captured the motion of fluorophores using high-speed imaging. The videos and individual frames where the motor was used showed significantly clearer images due to the enhanced motion provided by the modulation of the light ([Figure 3](high-speed-brownian-motion-capture-using-ebis.md#figures), [Supplemental Material 3](high-speed-brownian-motion-capture-using-ebis.md#supplemental-materials)). This was not as apparent in the non-motor condition ([Figure 2](high-speed-brownian-motion-capture-using-ebis.md#figures), [SM 2](high-speed-brownian-motion-capture-using-ebis.md#supplemental-materials)). The use of over accumulation marginally improved the clarity of the captured motion, suggesting that oversampling may be slightly beneficial in limited signal conditions. However, the increase in integration time sacrifices the real-time capability of the imaging process and increases overall noise in the image. These trade-offs are likely not worth the returns. Very little motion was captured as can be seen from supplemental material 1. This may be due to too much surface tension and not enough room between the coverslip and the well.

### Discussion

The imaging results demonstrated the effectiveness of using light modulation and oversampling techniques to improve the visibility of Brownian motion at high frame rates. The clear distinction between the motor-enabled and non-motor data sets emphasizes the impact of light modulation on imaging quality. Over accumulation appears  not to be a promising method for enhancing image clarity.&#x20;

Next steps should focus on refining the imaging process without the need for mechanical or temporal adjustments that can impede real-time analysis. The use of systematic optimization techniques, such as the Taguchi method, may offer a structured approach to enhancing SNR and potentially reduce the need for oversampling. This approach can systematically vary experimental parameters to find the optimal conditions for SNR improvement. Future experiments should also consider the impact of such enhancements on the ability to observe and measure rapid dynamic processes, which is critical for the accurate characterization of Brownian motion in various research and diagnostic applications.

Additionally it is worth trying other forms of encapsulating the fluorophores that is both repeatable and effective. It was mentioned that creating a well from Agar would be a potential alternative. It is also possible that the movement is not wide enough to trigger an event. This is possible considering the relatively large pixel pitch of the EBIS (15um).

### Figures

1.

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption><p>Brownian motion frame without motor</p></figcaption></figure>

2.

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption><p>Subsequent frame from fig 1. Negative event circled for clarity</p></figcaption></figure>

3\.

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption><p>Brownian motion experiment with motor</p></figcaption></figure>

4.

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption><p>No motor with over accumulation</p></figcaption></figure>

### Supplemental Materials

1\.

{% file src="../.gitbook/assets/motor_annotated_30fps.mp4" %}
30 FPS video visualizing brownian motion
{% endfile %}

2. 625 nm no motor 10kfps video currently unavailable
3. 625 nm motor 10kfps video currently unavailable
