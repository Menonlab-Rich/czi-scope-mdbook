# Deciphering Motion and Blinking in EBIS Using the Time Surface Algorithm

### **Introduction**

The EBIS's ability to capture extremely subtle changes in light intensity (down to 0.05 lux) and rapid events (up to 10,000 frames per second) is pivotal. This sensitivity makes it ideal for capturing both rapid motion and minute fluctuations in light intensity, like the intrinsic blinking of fluorescent dyes. Separating these events is crucial to understanding the output of the EBIS and visualizing the data correctly. This report introduces a method for handling this separation with simple motion. Further work is required to handle more complex situations.

### **Time Surface Algorithm - A Deeper Dive**:&#x20;

The time surface algorithm works by dividing some time span, $$\Delta{t}$$ second of data into $$dt$$ bins. By calculating the time difference in time between the last event and the start of each bin for every pixel, the algorithm creates a 'time surface' that reflects the recency of events. Summing these surfaces along the time axis gives a comprehensive picture of event frequency and recency across the entire time span, as seen in [fig 2](deciphering-motion-and-blinking-in-ebis-using-the-time-surface-algorithm.md#figures).

### **Experiment Insights: Blinking vs. Motion**

1. **Spatial-Temporal Correlation in Simple Motion**: The experiment's key insight lies in how it distinguishes between motion-induced and intrinsic blinking events. In simple motion, 'on' events precede 'off' events spatially, reflecting the direction of movement. This spatial lead-lag relationship is a signature of motion.
2. **Blinking Events Identification**: Blinking or flickering, in contrast, is characterized by a temporal separation of 'on' and 'off' events without spatial displacement. The algorithm identifies blinking by detecting overlapping 'on' and 'off' events in the same spatial region across time bins.
3. **Case Study - Fluorescent Bead Movement**: The experiment's scenario involving a moving fluorescent bead illustrates this concept. As the bead moves, it generates a trail of 'on' and 'off' events reflecting its path ([fig 1](deciphering-motion-and-blinking-in-ebis-using-the-time-surface-algorithm.md#figures)). However, if the bead also blinks, there will be instances where 'off' events temporally and spatially coincide with 'on' events, indicating blinking rather than motion. This is best visualized over time by summing the time bins along the t axis to create a single picture of the motion over time ([fig 2](deciphering-motion-and-blinking-in-ebis-using-the-time-surface-algorithm.md#figures)).

### **Overlap and Data Processing**

1. **Single Pixel Event Registration**: The fact that a single pixel can only register one event at a time -- "on" or "off" -- poses a challenge. The algorithm overcomes this by not correlating events by their exact timestamps but rather by their occurrence within the same spatial-temporal bin. This approach allows for the detection of overlapping events indicative of blinking.
2. **Data Binning and Correlation**: The use of time bins is crucial. It provides a framework to correlate events spatially and temporally, enabling the distinction between motion and blinking. This binning approach is a clever solution to the problem of overlapping event detection.

### **Challenges and Future Research Directions**

1. **Complex Motion Analysis**: The current approach is effective for simple motion patterns. However, complex scenarios with multiple moving objects or varying intensities might require more sophisticated algorithms or additional data processing techniques.
2. **Algorithm Optimization for Different Scenarios**: Tailoring the time surface algorithm for specific applications, such as biomedical imaging or industrial monitoring, could enhance its effectiveness and broaden its applicability.
3. **Integration with Machine Learning**: Incorporating machine learning techniques could improve the algorithm's ability to differentiate between motion and blinking, especially in complex and noisy environments.

### **Concluding Remarks**

The results indicate that the aforementioned algorithm offers a method to distinguish between intrinsic blinking and motion. This distinction is crucial in fields where accurate interpretation of dynamic visual data is essential. The approach, while effective, invites further refinement and exploration, particularly in handling more complex scenarios and integrating with other technological advancements.

### Figures

1.

    <figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption><p>Time surface separated by polarity depicting how negative events trail positive events</p></figcaption></figure>


2.

    <figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption><p>Time surface summed along t axis separated by blinking and motion</p></figcaption></figure>
