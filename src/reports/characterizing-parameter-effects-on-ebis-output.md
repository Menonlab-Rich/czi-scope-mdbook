# Characterizing parameter effects on EBIS output

### Key Points:

* **Objective**: Understanding the impact of various setup variables on an Event Based Image Sensor (EBIS).
* **Variables Tested**: Tuning parameters, laser power, motor usage, and ground glass diffuser.
* **Method**: Controlled experiments with fluorescent beads and different setup configurations.
* **Major Findings**:
  * Exponential relationship between event count and on/off threshold settings.
  * Influence of laser power on EBIS output and beam speckle.
  * Motor's impact on EBIS output.
  * Effectiveness of ground glass diffuser in beam speckle reduction.
* **Optimal Setup**: No motor with diffuser combination.
* **Improvements**: Implementation of a 90:10 splitter and adjustments in mirror alignment and magnification.

### Introduction:

This report details a series of experiments conducted to understand the impact of various variables on the output of an Event Based Image Sensor (EBIS). Using a controlled experimental setup involving fluorescent beads, the effects of tuning parameters, laser power, motor, and ground glass diffuser on the EBIS were meticulously investigated. The aim was to optimize the EBIS setup for enhanced performance and clarity.

### Experiments:

1. **Tuning Parameters**:
   * Method: Incremental adjustment of on-event thresholds while focusing on a fluorescent bead.
   * Observation: Exponential relationship between event count and threshold settings.
2. **Laser Power**:
   * Method: Varying laser power in 4mw steps, comparing EBIS output with CMOS readings.
   * Observation: Correlation between laser power and average intensity in EBIS and beam speckle in CMOS.
3. **Motor**:
   * Method: Assessing motor's effect on EBIS output using a silver slide and emission filter removal.
   * Observation: Detectable influence of motor-induced motion on EBIS.
4. **Ground Glass Diffuser**:
   * Method: Repeating motor experiment with a diffuser to analyze its effect on beam speckle.
   * Observation: Motor and diffuser combinations impact on EBIS and CMOS outputs.
5. **Comprehensive Characterization**:
   * Method: Testing motor/diffuser permutations on moving and static beads, recording EBIS and CMOS outputs.
   * Observation: Detailed characterization of motor and diffuser's effect on setup.

### Results:

The experiments revealed that the most effective setup for EBIS involves using no motor in conjunction with a diffuser. This setup minimized the issues related to beam speckle and event spike at the frame's edge. Further improvements, including a 90:10 beam splitter and alignment adjustments, yielded clearer results and minimized distortion when beads lost focus.

### Discussion:

The findings from these experiments are critical for enhancing EBIS performance. The exponential relationship between event count and threshold settings underscores the need for precise tuning of EBIS parameters. The motor, while useful for reducing beam speckle, was found to negatively impact the EBIS output, an issue resolved by the ground glass diffuser. The final setup adjustments, particularly the splitter ratio change and optical alignment, significantly improved the quality of the sensor's output.

### Figures

1.

    <figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
2.

    <figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>
3.

    <figure><img src="../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>


4.

    <figure><img src="../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>


5.

    <figure><img src="../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>


6.

    <figure><img src="../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>


7.

    <figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>
8.

    <figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>


9.

    <figure><img src="../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>


10.

    <figure><img src="../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>


11.

    <figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>


12.

    <figure><img src="../.gitbook/assets/vlc-record-2023-12-15-12h46m16s-vlc-record-2023-12-15-12h45m32s-625_fluorophore_no_motor_no_diffuser_moving.avi-.avi-.gif" alt=""><figcaption><p>As captured by the CMOS</p></figcaption></figure>


13.

    <figure><img src="../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>


14.

    <figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>


15.

    <figure><img src="../.gitbook/assets/vlc-record-2023-12-15-13h08m07s-vlc-record-2023-12-15-13h07m39s-625_motor_no_diffuser_moving.avi-.avi-.gif" alt=""><figcaption><p>As seen by the CMOS</p></figcaption></figure>
16.

    <figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>


17.

    <figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>


18.

    <figure><img src="../.gitbook/assets/vlc-record-2023-12-15-13h33m29s-625_diffuser_no_motor_moving.avi-.gif" alt=""><figcaption><p>As seen by the CMOS</p></figcaption></figure>
19.

    <figure><img src="../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>


20.

    <figure><img src="../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>
21.

    <figure><img src="../.gitbook/assets/vlc-record-2023-12-15-13h50m57s-625_motor_diffuser_moving.avi-.gif" alt=""><figcaption><p>As seen by the CMOS</p></figcaption></figure>


22.

    <figure><img src="../.gitbook/assets/image (131).png" alt=""><figcaption><p>With 90:10 splitter and corrected magnification</p></figcaption></figure>


23.

    <figure><img src="../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>


24.

    <figure><img src="../.gitbook/assets/2023-12-21-09-50-29_625_diffuser_no_motor_moving.gif" alt=""><figcaption><p>As seen by the CMOS (Due to exposure time requirements of the CMOS, nothing is visible until the bead stops moving)</p></figcaption></figure>
