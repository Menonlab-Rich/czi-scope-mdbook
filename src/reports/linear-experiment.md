---
description: Testing the linearity of the response with the 605nm fluorophore
---

# Linear Experiment

### Objective

To examine the linear behavior of a 605nm fluorophore under different excitation source powers and understand the challenges and observations related to its emission.

### Procedure

1. **Sample Preparation**: A dilute sample of 605nm fluorophore was placed on a glass cover slide and allowed to dry.
2. **Emission Direction**: The 90/10 beam splitter was removed, directing 100% of the emission to the CMOS camera.
3. **Laser Power Adjustment**: The laser power was increased to its maximum of 55mW.
4. **Focusing**: A small group of beads was brought into focus.
5. **Beam Splitter Replacement**: The 90/10 beam splitter was reinstalled and the output of the event camera was observed.
6. **Power Modulation**: The power of the excitation source was varied in steps from 0mW to 50mW.
7. **Data Collection**: At each power step, a sample was recorded and the events/sec value was retrieved.

### **Observations**

* A linear behavior of the fluorophore emission was observed between 10mW and 30mW of excitation power.
* Post the 10mW mark, there was no significant increase in signal intensity. However, between 40mW and 50mW, a noticeable rise in noise was seen, but not in the signal.
* Without any modulation, the signal value in the EBIS was extremely low, making it nearly unobservable. This observation suggests that if the falling edge of the laser cannot be used as the period of interest, an alternative modulation technique might be required.
* The suspicion that emission light was penetrating the sensor was confirmed. This was evident when the emission source could be seen on the CMOS camera even with the excitation filter in place. This observation was particularly prominent during the focusing step when the 90/10 splitter was removed and the excitation source was at full power.

### Additional Tests

A test was conducted where a signal was recorded at the off edge of the laser and then a noise image was subtracted from it. The result indicated that this approach could be effective if multiple signal images are averaged, thereby enhancing the Signal-to-Noise Ratio (SNR). Hence, conducting another test with multiple images seems a promising avenue to explore further.

### Figures



Signal, Noise, difference from 2nd experiment

![](<../.gitbook/assets/image (28).png>)

Events vs Power plot from 1st Experiment (Positive and Negative events considered)

![](<../.gitbook/assets/image (29).png>)

Excitation laser visible atop unfocused red fluorophore

![](<../.gitbook/assets/image (30).png>)

Focused cluster of fluorophores used for first experiment

![](<../.gitbook/assets/image (31).png>)

Dichroic Transmission Plot

![](<../.gitbook/assets/image (13).png>)

### **Attachments**

* Transmission spectra of the dichroic.

{% file src="../.gitbook/assets/MD588.xlsx" %}
Transmission Spectra
{% endfile %}
