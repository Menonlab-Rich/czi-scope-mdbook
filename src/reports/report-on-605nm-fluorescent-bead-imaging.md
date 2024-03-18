---
description: Authored 10/05/23
---

# Report on 605nm Fluorescent Bead Imaging

### Key Points

* Dilution of the 605nm fluorescent beads by 2x allowed for individual bead focus.
* Meticulous tuning of the EBIS parameters isolated the desired signal from noise.
* The recorded sequence captured the laser oscillating between power states.
* Temporal integration and noise thresholding led to discernible spatial patterns in the resultant images.
* Pearson correlation coefficient indicated significant spatial differentiation in the DFA, signaling potential for higher resolutions.

### Abstract:

Fluorescent beads present an opportunity for studying optical properties and imaging characteristics. In this study, a 605nm fluorescent bead is isolated and observed through the EBIS behind a DFA. The resultant image, and the event stream that produced it is analyzed using a variety of statistical methods. The spatial correlation between two arbitrary points within the FOV is measured and next steps are considered.

### Experimental Procedure:

1. **Bead Preparation**: The 605nm fluorescent beads [previously](updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md) diluted, were further diluted by 2x to enable focusing on an individual bead (See [Figure 1](report-on-605nm-fluorescent-bead-imaging.md#figures)).
2. **EBIS Tuning**: Parameters of the EBIS were meticulously adjusted according to the [SOP](../guides/understanding-and-tuning-the-prophesee-evk-3-event-camera.md). The aim was to isolate the signal from the laser drop-off and minimize noise.
3. **Recording**: A sequence was captured of the laser oscillating between 8mW and 0mW power, completing four cycles. Both positive and negative events were segregated with positive ones being discarded. Without altering the camera tuning settings, the bead was relocated, and the recording procedure was reiterated.

### Results:

* **Time Series Analysis**: The time series of the events, as illustrated in [Figures 2 and 3,](report-on-605nm-fluorescent-bead-imaging.md#figures) clearly showcases that the negative spikes surpass the noise threshold, indicating a distinguishable signal for processing.
* **Temporal Integration**: Events from both recordings underwent temporal integration into spatial frames at $$\delta{t}$$ = 1ms. Slices that did not surpass the noise threshold were discarded, and the survivors were averaged to produce the final image (refer to [Figure 4](report-on-605nm-fluorescent-bead-imaging.md#figures)). The image reveals a central cluster of events, indicative of a structure from the DFA, albeit with some edge-spreading.
* **Spatial Differentiation**: Both images were cropped to focus on the primary structure, as depicted in [Figure 5](report-on-605nm-fluorescent-bead-imaging.md#figures). Their comparison using the Pearson correlation coefficient yielded a correlation of 0.035, suggesting distinct spatial differentiation in the DFA, a precursor to achieving higher resolutions.

### Discussion:

The promising results from the 605nm fluorophore pave the way for subsequent experimentation with the 625nm fluorophore. However, there are considerations to bear in mind:

* **Tuning Parameters**: The events were optimized with the 605nm fluorophore as the primary focus. It's essential to maintain these tuning parameters consistent across experiments to ensure valid comparisons. Any deviation might necessitate repeating the 605nm fluorophore imaging.
* **Potential Adjustments**: The appearance of another signal in the top right corner of Figure 2, likely another fluorophore outside the CMOS camera's field of view, suggests the possibility of employing a lens with a shorter focal length to further condense the excitation beam.

### Conclusion:

The process successfully highlighted the capabilities of the EBIS system in imaging the 605nm fluorescent bead with discernible differentiation. The subsequent steps involve replicating the experiment with the 625nm fluorophore and drawing meaningful comparisons to understand the variations with respect to wavelength.

### Recommendations:

1. Ensure consistent tuning parameters across experiments to draw valid comparisons.
2. Consider the utilization of a lens with a shorter focal length to achieve a more focused excitation beam.

### Figures

1.

    <figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption><p>A single flurophore as seen through the CMOS camera</p></figcaption></figure>


2.

    <figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption><p>Signal data - First Image pre move</p></figcaption></figure>


3.

    <figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption><p>Signal data - second image post move</p></figcaption></figure>


4.

    <figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption><p>Integrated Frame - First image pre move</p></figcaption></figure>


5.

    <figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption><p>Integrated Frame - Cropped to the central structure</p></figcaption></figure>
