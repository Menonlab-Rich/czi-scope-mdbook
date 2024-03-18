# Analysis of Laser Light Leakage and Its Impact on EBIS Detection: Troubleshooting and Recommendation

### Highlights

* The setup does not allow the dichroic to be held perfectly at 45deg allowing some laser light to pass through
* This is visible in the cmos and the EBIS when the emission filter is removed.
* Regardless of the position of the emission filter (in front of the sensor or in the column) enough laser light is transmitted through the filter to be detected on the EBIS

### **Experiments**

_Note: All results from the EBIS are from experiments with the excitation filter in place and all bias settings left at default_

1. 1.Excitation beam focused on the resolution chart
   * Procedure
   * The Excitation source was powered to 2mw
   * The resolution chart was focused using the CMOS with the dichroic mirror in place and the emission filter removed.
   * The emission filter was replaced
   * In the EBIS gui it was observed that the number of events increased by 150% from a baseline of 4000 events/s to 10000 events/s
   * It was further observed that despite this increase, no image was detected in either the CMOS or the EBIS.
   * The emission source was abruptly powered down
   * Results
   * It was noted that the dichroic did not block all of the excitation source
   * Upon powering down the laser a large spike of negative events occurred in the region where the excitation source was focused.
2. 2.Excitation beam focused onto a glass slide

* _Note: This experiment was performed twice. The first time the results were inconclusive. The second time the results were as stated. It is believed the difference between the first and second attempts was the level to which the beam was focused, being greater in the second case._
  * Procedure
  * The Excitation source was powered to 2mw
  * A glass slide of the same kind used in fluorescent samples was placed beneath the objective
  * Using a small slice of paper in front of the EBIS, the source was focused to a tight point
  * With the emission and dichroic filters in place the emission source was abruptly powered down
  * Results
  * Upon powering down, a large spike in negative events were observed in the location where the emission source was focused.

1. 3.Moving the emission filter
   * Procedure
   * Experiment 1 was repeated with the same parameters, holding the emission filter in place in front of the sensor to determine whether the issue was resultant from ambient light or directed light.
   * Results
   * The results from experiment 1 were reproduced exactly as previously documented.

**Conclusion** Given that in every case, the observed events upon turning off the shutter were focused in the same region that the emission source was observed to be focused, it can be concluded that the source of the events is not ambient transmittance from the emission source, but directed light through the emission filter. This is further confirmed by the third experiment where moving the filter was shown to have no effect.​

### Figures

**left to right, top to bottom:** Empty slide experiment from EBIS perspective, Resolution Chart experiment from EBIS perspective, Empty slide experiment from CMOS perspective, Resolution Chart experiment from cmos perspective

​**Note:** The cmos images are taken without the emission filter before the laser is turned off. The EBIS images are taken with the emission filter as the laser is turning off.

![](<../.gitbook/assets/image (23).png>)![](<../.gitbook/assets/image (24).png>)

![](<../.gitbook/assets/image (25).png>)![](<../.gitbook/assets/image (26).png>)
