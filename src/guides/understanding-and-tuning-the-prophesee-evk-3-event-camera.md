# Understanding and Tuning the Prophesee EVK-3 Event Camera

***

### Introduction

The Prophesee EVK-3 evaluation kit represents the forefront of event-based imaging. Unlike conventional cameras, this unique device responds exclusively to changes in a scene, bringing efficiency and precision to diverse applications.

***

### Camera's Three-Stage Design

1. **Photodiode Detection**: Converts incoming light into voltage through a logarithmic converter.
2. **Filtering**: Comprises:
   * **Temporal Band-Pass Filter**: Signals outside a specific temporal frequency range are dismissed.
   * **Contrast Detection**: Signals, based on their intensity difference, are channeled to 'on' or 'off' comparators.
3. **Output Stage**: The comparators' data advances to the arbiter, which then processes the voltages and dispatches the results via USB for subsequent processing.



### Thinking Analog: The Filtering Perspective

Consider the event stream as an ongoing analog signal rather than discrete moments. This perspective facilitates the application of standard signal processing techniques, providing clarity to the tuning process.

***

### Bias: The Heart of Performance

A variety of tunable biases directly influence camera performance:

* **Bias\_pr**: Governs the photoreceptor, primarily impacting the photodiode's operating point. Typically, it's best left untouched.
* **Bias\_fo**: Adjusts the pixel's low-pass cut-off frequency, balancing bandwidth and noise (see figures (see figures).
* **Bias\_hpf**: Modifies the high-pass cut-off frequency, aiming to exclude slower events, especially in dim light (see figures).
* **Bias\_diff**: Sets the comparator's reference voltage. While usually left unchanged, adjustments might be necessary for ultra-low latency applications.
* **Bias\_diff\_on** and **Bias\_diff\_off**: These control the comparators' thresholds, with their difference determining the camera's contrast sensitivity. Fine-tuning these settings is critical, given their pronounced effect on performance. When intensity crosses a threshold, the pixel resets. This reset duration, essential to prevent redundant event registration, is influenced by the bias\_refr setting (See figures). The event probability concerning temporal contrast, depicted in percentage units as $$C=\frac{I_\text{high} - I_\text{low}}{I_\text{low}}\times100$$, is also influenced by these biases. This relationship highlights how bias\_diff\_on and bias\_diff\_off govern the chances of event registration for a given contrast level (see figures).
* **Bias\_refr**: Manages the refractory period, a post-event "blind" interval, curtailing redundant event registration. The plot below provides a relationship between the bias\_refr setting and the refractory period (see figures).

***

### Tuning Methodology

**The Goal amd Process**: The goal of bias tuning is to achieve the highest event rate possible while minimizing noise and redundant event registration. What follows is a step-by-step guide to achieving this goal. The tuning process is iterative, with each step building on the previous one. A first pass should be performed in the order below, while subsequent passes can be performed to individual biases as needed.

1. **Ambient Control**: Mastery over ambient light is pivotal. The sensor's acute sensitivity, beneficial in dim conditions, also renders it prone to saturation. Protective measures are paramount. Consider any light source that might impact the camera's performance, including lamps, monitors, shadows, and reflections. To this end, baffling and shielding are essential. Ensure that the baffles used are in no way reflective.
2. **Temporal Filters Calibration**: Once ambient light is under control, the temporal filters can be tuned. The goal is to set the high-pass filter's cut-off frequency to exclude slow events while the low-pass filter's cut-off frequency should be set to the period of the fastest event of interest. For instance, if the fastest event of interest occurs every 10 ms, the low-pass filter's cut-off frequency should be set to 100 Hz. Refer to the plots above for guidance. Begin by adjusting the high-pass filter's frequency. Lower the bias\_hpf setting until there are no more visible positive events (at this stage there may still be some negative events). Then increase the bias\_hpf settings until the positive events reappear. Continue increasing this value until noise begins to appear. At this point, the high-pass filter's cut-off frequency is set. Next, adjust the low-pass filter's cut-off frequency. Lower the bias\_fo setting until the image as seen in the viewer software begins to degrade. Then increase the bias\_fo setting until the image is restored. Continue increasing this value until noise begins to appear. At this point, the low-pass filter's cut-off frequency is set.

**Note**: At this stage, the object of interest may not be clearly visible. This is okay. The goal is to set the temporal filters to exclude unwanted events. The object of interest will become visible in the next step.

3. **Contrast Detection Thresholds Tuning**: Once the temporal filters are set, the contrast detection thresholds can be tuned. The goal is to limit the contrast detection thresholds to the minimum values that still allow the object of interest to be visible. As the camera is more sensitive to off events than on, begin by lowering the bias\_diff\_off setting until there are no more visible negative events. Then increase the bias\_diff\_off setting until the negative events reappear. Continue increasing this value until the object of interest is clearly visible. At this point, the bias\_diff\_off setting is set. Next, adjust the bias\_diff\_on setting. Increase the bias\_diff\_on setting until there are no more visible positive events. Then decrease the bias\_diff\_on setting until the positive events reappear. Continue decreasing this value until the object of interest is clearly visible. At this point, the bias\_diff\_on setting is set.

**Note**: If the object of interest is still not clearly visible, the temporal filters may need to be adjusted. If the object of interest is still not clearly visible after adjusting the temporal filters, the contrast detection thresholds may need to be adjusted again. This process may need to be repeated several times.

4. **Refractory Period Adjustment (If Necessary)**: Should the camera detect multiple events for a single intensity change, it might be necessary to extend the refractory period. Refer to the plot above for guidance.

### Everyday Frequency Modulations

When tuning, accounting for commonplace modulation frequencies is paramount. Given that many light sources may exhibit 120 Hz flicker due to the US's 60 Hz alternating current frequency, recognizing such patterns is crucial. Other potential flicker sources include monitor refresh rates and specific LEDs. Such awareness prevents unwelcome artifacts and aliasing effects.

### A quantitative guide to temporal filters

The guide above provides a solid qualitative guide to tuning the filters. However, a quantitative guide is also useful. Though there exists little documentation on the qualitative nature of the contrast filters, the temporal filters are well documented. For periodic motion, the temporal filters can be tuned to the period of the motion, using the plot above as a guide. For aperiodic motion, the temporal filters can be tuned to the velocity of the motion.

**Tuning for aperiodic motion**

Consider an object moving at a constant velocity $$( V_{\text{object}})$$. Given that the image formation occurs through a lens with a known magnification factor $$( M )$$, the image velocity becomes $$( V_{\text{image}} = M \times V_{\text{object}} )$$. Now, consider a single pixel on the camera's sensor. As the object traverses the pixel's field of view in time ( $$t$$ ), the pixel experiences an intensity change of magnitude $$( \Delta I )$$. If the low-pass cutoff frequency of the pixel's band-pass filter is set between $$1/t$$ and $$2/t$$, an event won't be registered at time $$t/2$$ since the intensity change over this duration doesn't meet the filter's threshold. However, by time $$t$$, the intensity change meets or surpasses the filter's sensitivity, leading to event registration.

This illustrates that even for non-periodic motion, the settings of the band-pass filter influence the rate at which events are detected and registered by the sensor. The plot below depicts this scenario.

**Finding the period of a periodic signal**

If the signal appears periodic, Prophesee provides a sample application for estimating the period of the signal. The application can be found in the Prophesee SDK under the `samples` directory. Refer to the [documentation](https://docs.prophesee.ai/stable/samples/modules/analytics/vibration\_py.html?highlight=vibration%20estimation) for more information.



### Figures

![](<../.gitbook/assets/image (17).png>)![](<../.gitbook/assets/image (18).png>)![](<../.gitbook/assets/image (19).png>)![](<../.gitbook/assets/image (20).png>)![](<../.gitbook/assets/image (21).png>)![](<../.gitbook/assets/image (22).png>)
