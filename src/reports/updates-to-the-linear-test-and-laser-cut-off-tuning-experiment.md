---
description: 'Authored: 10/03/2023'
---

# Updates to the Linear Test and Laser Cut-off Tuning Experiment



***

### **Linear Test Updates**

The linear test was conducted following standard procedures. The process is outlined as follows:

1. **Beam Splitter Adjustment**: The 90/10 beam splitter was removed from the optical path. This adjustment was made to ensure that 100% of the emission was directed to the CMOS.
2. **Sample Preparation**: A dilute sample of 605nm fluorophore was carefully placed on a glass slide and allowed adequate time to dry.
3. **Laser Power**: The 561nm excitation laser was set to a power level of 10mW.
4. **Focusing the Sample**: Using the CMOS, the sample output was brought into focus (refer to [Figure 2](updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md#figures) for the visual output).
5. **Reinstallation of the Splitter**: The 90/10 splitter was duly replaced in its original position.
6. **Power Adjustment**: The laser's power was incremented in 2mW steps, starting from 0mW (representing the noise floor) and reaching up to 20mW.
7. **Recording Output**: At every power increment, a dedicated recording was made of the output of the EBIS.
8. **Event Segregation**: The recorded events were separated into positive and negative events.
9. **Event Rate Calculation**: For each power level, the rate of events per second was computed for both positive and negative events.

#### Results

The results from this test align with [prior observations](linear-experiment.md). Specifically, there's a linear increase in the number of events from 0mW up to 10mW. The detailed results can be viewed in [Figure 1](updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md#figures). The red lines in this figure demarcate the sections where the number of events exhibited strict monotonic increment.

### Laser Cut-Off Tuning

For this experiment, the laser was adjusted to 8mW in accordance with the findings from the linear test. A compact cluster of fluorescent beads was visualized through the event camera. It's worth noting that the same set of fluorescent beads was employed for both this and the linearity tests. However there's no stringent need to use the same beads.

The event-based imaging system (EBIS) of the camera was tuned in line with the [standard operating procedure](../guides/understanding-and-tuning-the-prophesee-evk-3-event-camera.md) (SOP). The primary focus of this tuning was threefold:

1. Minimize the positive events.
2. Maximize the event signal on the falling edge of the excitation laser.
3. Ensure minimal leakage from the excitation.

During the experiment, the laser's power was cyclically modulated between 8mW and 0mW, for a total of 5 cycles. The raw file obtained from these cycles was integrated with a time step $$( \Delta t )$$ of 100 microseconds.&#x20;

#### Results

The visualization of the results can be found in [Figure 3.](updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md#figures)\


### Conclusion

The results from the [#linear-test-updates](updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md#linear-test-updates "mention") suggests that the best power level for imaging is between (0, 10]mW. This is in line with [previous findings](linear-experiment.md#observations) that suggest that at sufficiently high power levels excitation leakage can wash out relevant fluorescent signals.\


The results from the [#laser-cut-off-tuning](updates-to-the-linear-test-and-laser-cut-off-tuning-experiment.md#laser-cut-off-tuning "mention") suggests that it is possible to use the falling edge of the laser to retrieve the signal from the EBIS. The challenge will arise due to the briefness of the signal. When integrating, several cycles are required to get a detailed image. This will require a significant amount of time given the  long rise time of the laser. \
\
It should also be noted that the tuning experiment used a different set of tuning parameters than was used for linearity test. It should be confirmed, once the final tuning parameters have been dialed in, that there exists a linear region for the calibration to operate in.



### Figures

1. ![](<../.gitbook/assets/image (10).png>)
2. ![](../.gitbook/assets/linear\_test\_2\_603nm.jpg)
3. ![](<../.gitbook/assets/image (9).png>)

### Addendums

* 10/4/23: Image 3 was updated to accurately reflect the integrated events from the EBIS. See [EBIS Stuck Pixel](../documentation/ebis-stuck-pixel.md) in the documentation for further explanation.
