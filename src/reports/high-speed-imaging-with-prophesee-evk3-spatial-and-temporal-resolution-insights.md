---
description: Authored 11/01/2023
---

# High-Speed Imaging with Prophesee EVK3: Spatial & Temporal Resolution Insights

### Key Points

* Integration time for each recording was determined as $$\frac{1}{\text{FPS}}\times{1\times{10^6}}\mu{\text s}$$.
* Results show discernable signals at every frame rate, with diminishing signals at higher frame rates.
* The Prophesee EVK3 can achieve high spatial and temporal resolution simultaneously.

### Experimental Setup

1. Prepare a fresh dilute sample of the 625nm fluorophore on a glass slide.
2. Place the sample under the objective.
3. Remove the DFA from the event camera path.
4. Temporarily remove the 90/10 beam splitter to direct all light to the CMOS camera.
5. Locate a single fluorophore in the field of view.
6. Measure the fluorophore using the full wave at half power method.
7. Replace the beam splitter to direct light toward the event camera.
8. Tune the event camera according to the [SOP](../guides/understanding-and-tuning-the-prophesee-evk-3-event-camera.md).
9. Start the laser modulation at a peak of 5mW and record several oscillations.
10. Repeat the process with a peak of 8mW.
11. Load the recordings into Metavision Studio and isolate a single oscillation.
12. Export recordings at frame rates of 500fps, 1000fps, 3000fps, 5000fps, 7000fps, and 10000fps for both 5mW and 8mW versions, with integration time given as $$\frac{1}{\text{FPS}}\times{1\times{10^6}}\mu{\text s}$$.

### Results

Upon analyzing the recordings, a discernible signal was observed at every frame rate. However, as the frame rate increased, the signal strength diminished progressively. This suggests that while high frame rates are achievable, there is a trade-off in signal strength.

### Discussion

The experiment successfully demonstrated the capability of the Prophesee EVK3 to achieve both high spatial and temporal resolution simultaneously. The diminishing signal strength at higher frame rates is expected due to the reduced integration time, which results in less light being captured per frame. This trade-off between frame rate and signal strength is a common challenge in high-speed imaging.

The results also emphasize the importance of optimizing the laser power and modulation settings to achieve the best balance between resolution and signal strength. The difference in signal strength between the 5mW and 8mW peaks could be further investigated to determine the optimal laser power for this specific application.

Next steps could involve:

1. Exploring different fluorophore concentrations to see if a stronger signal can be achieved without compromising resolution.
2. Investigating the use of different beam splitters or optical components to enhance light collection efficiency.
3. Conducting a detailed analysis of the signal-to-noise ratio at different frame rates to determine the practical limits of the system.
4. Exploring advanced post-processing techniques to enhance the signal in high frame rate recordings.

Overall, the experiment provides valuable insights into the capabilities and limitations of the Prophesee EVK3 in the context of high-speed fluorescence imaging.

### Supplemental Materials

{% file src="../.gitbook/assets/625_fluorophore_modulated_5mw_1000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_5mw_3000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_5mw_5000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_5mw_7000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_5mw_10000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_8mw_500fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_8mw_1000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_8mw_3000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_8mw_5000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_8mw_7000fps_no_dfa.avi" %}

{% file src="../.gitbook/assets/625_fluorophore_modulated_8mw_10000fps_no_dfa.avi" %}
