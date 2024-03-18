---
description: authored 10/9/2023
---

# DFA, 4F, and EBIS adjustments

### Key Points

* Adjustment of the 4F to correct magnification is critical to obtaining precise imaging.
* DFA adjustment is necessary to achieve the desired magnification difference between EBIS and CMOS images.
* EBIS sensor tuning parameters differ for the 605nm and 625nm fluorophores, influencing image clarity and precision.

### Abstract

The report investigates the importance of adjusting the 4F system, the DFA, and the tuning parameters of the EBIS sensor when working with different fluorophores. These adjustments ensure accurate magnification and quality of the produced images.

### **Experimental Procedure**

1. **4F System Adjustment**:
   * The 4F system was reverted to its initial position.
   * Magnification was verified using a resolution chart comparing both the CMOS and EBIS paths.
2. **DFA Adjustment for EBIS Imaging**:
   * Using a 10Hz strobing light with the 90/10 beam splitter, EBIS imaging was initiated.
   * The DFA position was adjusted to achieve an image with approximately three times the size of the one captured on the CMOS.
3. **EBIS Sensor Tuning for Different Fluorophores**:
   * Initially, settings for imaging a 605nm fluorophore were established.
   * These settings were then used as a baseline to compare with the 625nm fluorophore.
   * Necessary adjustments were made based on the intensity and clustering observations.

### Results

1. **4F System Adjustment**:
   * Both CMOS and EBIS yielded magnifications close to the theoretical 40x, with CMOS at 39.2x and EBIS at 38.9x.
2. **DFA Adjustment**:
   * Post-adjustment, the EBIS image showed about three times the size of the CMOS image, with minimized blurring.
3. **EBIS Sensor Tuning**:
   * The 625nm fluorophore produced no signal on the EBIS with the settings chosen for the 605nm fluorophore. This required readjustments.
   * Post-adjustment, EBIS captured more 625nm fluorophores and clusters than the CMOS did.

### Discussion

The process of adjusting both the 4F system and the DFA plays a paramount role in determining the quality and magnification of the images produced. The 4F system's adjustment brought both the CMOS and EBIS paths closely aligned with the theoretical 40x magnification, which is a testament to the system's precision. However, slight discrepancies between these measurements, even if minute, might affect certain high-precision applications.

Adjusting the DFA was another critical step in the experimental process. The target was to produce an image on the EBIS that was approximately three times the size of the CMOS image. Achieving this is significant as it allows for higher detail capture, while assuring enough blurring exists to differentiate between wavelengths.

Furthermore, the nuances between the 605nm and 625nm fluorophores presented challenges. The 625nm fluorophore exhibited a reduced intensity compared to the 605nm when using similar EBIS sensor tuning parameters. This not only underscores the sensitivity of the EBIS sensor but also emphasizes the importance of fine-tuning the sensor parameters according to the specific fluorophore in use. The clustering phenomenon observed with the 625nm fluorophore at 1% concentration suggests further dilution will be required to image a single flurophore.

### **Conclusion**

Adjusting the 4F system was completed without issue. DFA adjustments were adjusted without issue as well. The EBIS sensor tuning needs to be set to acommodate multiple different fluorophores, as settings optimal for one fluorophore may not be suitable for another.

### **Next Steps**

1. Explore optimal dilution methods for the 625nm fluorophore to reduce clustering.
2. Investigate the possibility of creating a universal tuning parameter set for the EBIS sensor across various fluorophores.
3. Analyze the relationship between DFA adjustment and the clarity of the resulting images on different imaging paths

### Figures

**NOTE: I am currently unable to connect to the lab remotely. I will update this report with figures tomorrow, 10/10/23.**

***
