---
description: 'Authored: 11/13/2023'
---

# Comparative Analysis of Frequency Filtering approaches

### Key Points:

* Developed two code versions for filtering motor-generated noise in laser speckle mitigation.
* First approach: Time-domain analysis using vendor libraries, tracking x,y,p tuples, and filtering specific frequency ranges.
* Second approach: Fourier analysis to remove frequencies directly from frequency domain, with reconstitution of time series post-filtering.
* Fourier analysis identified 300-500Hz as the dominant noise frequency, matching vendor's frequency estimation.
* Time-domain filtering showed better results than Fourier analysis.
* Filtering showed minimal effect on signals without the motor, indicating the effectiveness of the filter on motor-induced noise.

### Experimental Setup:

1. Wrote first code version using vendor libraries for time-domain analysis, tracking x,y,p tuples, and measuring consecutive events to determine the period.
   1. This approach Implements frequency filtering with a time window parameter and a threshold for frequencies.
2. Developed second code version for frequency domain analysis using Fourier transformation.
   1. Grouped signal by (x,y,p) values, performed Fourier transform, filtered specific frequencies, and then applied inverse Fourier transform.
3. Ungrouped the time series to consider each (x,y,p,t) event for frame creation.

### Results:

The Fourier analysis identified a dominant frequency range of 200-500Hz ([Fig 1](comparative-analysis-of-frequency-filtering-approaches.md#figures)), consistent with the vendor's time-domain frequency estimation. The range of filtered events was chosen to be a high pass filter with a cutoff of 500Hz. This was performed using both approaches, however, the Fourier filter approach yielded poorer results compared to the time-domain analysis. When applied to data without the motor, the filtering had little to no effect, confirming the filter's specificity to motor-induced noise. The filtered data from the running motor still showed a significantly stronger signal than the data without the motor.

### Discussion:

The comparative analysis of the two approaches - time-domain and Fourier analysis - highlighted the effectiveness and limitations of each method in filtering motor-generated noise. The time-domain approach, with its focus on event sequences and frequency thresholds, proved more effective in mitigating noise, as evidenced by the stronger signal retention compared to the Fourier method. The consistency between the identified dominant frequency range in both methods (300-500Hz) reinforces the accuracy of the noise characterization.

The minimal impact of filtering on non-motor data underscores the filter's targeted effectiveness. However, the persistence of a stronger signal in motor-involved data, even post-filtering, suggests room for further refinement in the noise mitigation process.

Moving forward, the focus will shift to applying these filtering techniques to capture motion in different experimental setups - Brownian motion of fluorophores in liquid and capillary motion. The capillary experiment, involving the flow of fluorescent beads, is anticipated to yield quicker motions and potentially stronger signals, providing a different context to evaluate the effectiveness of the developed filtering approaches. The success of these experiments will hinge on the accurate setup and execution, along with the ability of the filtering methods to adequately reduce noise while preserving the integrity of the motion signal.



### Figures

1.

    <figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Fourier Frequency Analysis of Positive Events</p></figcaption></figure>

### Supplemental Materials

1. [Static Fluorophore Motor Fourier Filtering](https://drive.google.com/file/d/1xCv-oLMe4eT6Z6xLyMgZx96gHoHd\_zfZ/view?usp=drive\_link)
2. [Static Fluorophore Motor Time Domain Filtering](https://drive.google.com/file/d/1uxvHh8d-qWqgp1QBlkEwvvioKYLbxYeS/view?usp=drive\_link)
3. [Static Fluorophore No Motor Fourier Filtering](https://drive.google.com/file/d/1xYYWEpMuNnlyZciSJLmSHi9OEe9BGi2j/view?usp=drive\_link)
4. [Static Fluorophore No Motor Time Domain Filtering](https://drive.google.com/file/d/1FMwEpPae5Prju19dfxGOdPNKE8M4m7qL/view?usp=drive\_link)

