# Status Report 3/12/24

## **Completed Tasks:**

1. **Resnet Model Design Completion:** The design phase for the Resnet model is complete. This model can perform binary and n-object classifications.
2. **Focusing Algorithm Development:** Developing a focusing algorithm using z-stack methodology is underway. Initial research on a machine learning model to enhance focusing efficiency has started.
3. **Integration with Thorlabs APT:** Integration of Python with the Thorlabs APT shared library is complete, facilitating control over all Thorlabs motorized devices via a single interface.
4. **Zelux Camera Interface Development:** Ongoing development for interfacing with the new Zelux camera, targeted to be completed by EOD March 12, 2024.
5. **Optical Flow Verification:** Verified optical flow capabilities at high temporal resolution, implementing noise filtering techniques to enhance accuracy.

## **Next Steps:**

1. **Dataset Acquisition:** Capture a dataset using the new camera, employing a Thorlabs motorized filter slider to acquire images with and without the diffractive filter. Aim for a minimum of 2,000 images, varying the beads spatially and in concentration.
2. **Resnet Application for Bead Classification:** Apply the Resnet model to classify the color of beads using images obtained with the diffractive filter, starting with binary classification.
3. **Pix2pix Image Conversion:** Utilize Pix2pix to convert images from diffractive filter array (DFA) to standard image formats, using pairs captured in step 1.
4. **Integration of Optical Flow Data:** Capture motion data using the EBIS optical flow capabilities. Integrate color information from the Resnet classifier and convert DFA images to standard CMOS images using Pix2pix.
5. **System Testing with Single-Color Beads:** Test the setup on single-color beads to verify speed, accuracy, and color information. Conduct this test using the capillary experiment setup.
