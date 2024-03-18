---
description: Authored 10/11/23
---

# Comparison 605nm and 625nm fluorophores

### Key Points

* The concentration of fluorescent beads was diluted for both samples to facilitate finding a single fluorophore in the FOV.
* 605nm and 625nm fluorophores were separately imaged under the EBIS, taking care to locate both in the same position in the frame.
* A set of parameters was found that facilitates an image from both samples.
* The 625nm sample produces significantly more signal than does the 605nm sample

### Abstract

This report investigates the spatiospectral response of the DFA as viewed through the EBIS. Care is taken to ensure that the samples are imaged in the same location for each sample, and biases chosen to produce sufficient signal for both samples. The results are compared and implications discussed.



### Experimental Procedure

**605nm fluorophore**

* A dilute sample of the 605nm sample is placed on a glass slide and allowed to dry. A coverslip is placed over the top of the dried sample and both are placed under the objective.
* The 90/10 beam splitter is removed from the setup, allowing all the light to pass toward the CMOS. This is done strictly for focusing purposes.
* Virtual grid lines are overlaid on the CMOS output to facilitate exact placement.
* A single fluorophore is brought into focus and placed at the intersection of two grid lines ([Fig 1](comparison-605nm-and-625nm-fluorophores.md#figures)).
* The 90/10 beam splitter is replaced and the excitation laser is set to modulate between 8 and 0 milliwatts.
* Tuning parameters are adjusted until a clear structure is visible within the bead on the EBIS.
* Several oscillations are recorded and integrated into a single frame, discarding any frames that do not rise above a set noise threshold ([Fig 3](comparison-605nm-and-625nm-fluorophores.md#figures)).

**625nm fluorophore**

* The same process is followed to focus the 625nm as the 605nm sample.
* The focused bead is placed at the intersection of the same gridlines as the 625nm sample ([Fig 2](comparison-605nm-and-625nm-fluorophores.md#figures)).
* The biases are set to the exact settings used to image the 605nm sample.
* The 90/10 beam splitter is once again replaced and the excitation laser set to modulate between the same 8 and 0 milliwatts.
* Several oscillations are recorded after the same fashion as the 605nm sample ([Fig 4](comparison-605nm-and-625nm-fluorophores.md#figures)).

### Results

The results indicate a stronger response from the 625nm signal than from the 605nm laser. Crucially, fewer structural details are visible in the 625nm signal due to saturation. On the one hand, since the responses are so significantly different, this may be acceptable, however it is important to understand what the cause of the difference is exactly. Additional work is required to ensure that the results we are getting are acceptable to move forward with a full calibration.

### Discussion

There may be several reasons for the discrepancy of signal intensity between the two fluorophores, all other things being equal. More likely the true reason is a combination of these factors.&#x20;

1. This result may simply be a function of the DFA and its differing spectral response between the two wavelengths.
2. The 605nm fluoropores (Thermofisher InSpeck™ Red) have a specified bead size of 2.5$$\mu\text{m}$$ whereas the 625nm fluorophores (Cospheric FMMG - Magenta )  have a specified size of between $$[1, 5]\mu\text{m}$$, the one being used for this experiment measuring at approximately $$4\mu\text{m}$$. This is just shy of 2x the size and could account for the discrepancy.
3. The intensity response of the 605nm fluorophore is measured in relative percentages, whereas the 625nm fluorophores are measured in units of au. Thus it is difficult to compare their intensities directly. Nothwithstanding, it is possible that the 625nm fluorophore has a more intense response to excitation than does the 605nm ([Fig 5](comparison-605nm-and-625nm-fluorophores.md#figures))([Fig 6](comparison-605nm-and-625nm-fluorophores.md#figures)).

### Figures

1.

    <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>InSpeck™ Red (580/605) fluorophore (before precise positioning)</p></figcaption></figure>


2.

    <figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>FMMG - Magenta fluorophore (positioning grid lines shown)</p></figcaption></figure>


3.

    <figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>InSpeck™ Red (580/605) fluorophore - EBIS</p></figcaption></figure>


4.

    <figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>FMMG - Magenta fluorophore - EBIS</p></figcaption></figure>


5.

    <figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption><p>InSpeck™ Red (580/605) Spectra</p></figcaption></figure>


6.

    <figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>FMMG - Magenta Spectra</p></figcaption></figure>
