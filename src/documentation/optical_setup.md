# Optical Setup

**Laser Source and Initial Pathway**:

* The optical path begins with a 561nm continuous diode laser, serving as the excitation source.
* This laser is directed towards a planoconvex back focal length (BFL) lens with a focal distance of 50mm.

**Reflection and Direction**:

* Post the BFL lens, the laser beam is reflected downwards using a dichroic mirror (Thorlabs MDF88).
* This mirror is positioned at a 45-degree angle, securely held by a Thorlabs CM1-DCH - 30 mm Cage Cube equipped with a Dichroic Filter Mount.
* _Note_: A transmission graph for the dichroic mirror can be found below.

**Objective and Sample**:

* After being reflected by the mirror, the beam continues its path through a 40x objective, ultimately illuminating the sample.

**Reflected Excitation Path**:

* The light reflected from the sample travels upward, passing through the tube lens which focuses the columnated beam.
* This light then traverses a long pass filter (Thorlabs FELH0600) that operates with a cuton wavelength of 600nm.

**Beam Splitting and Final Pathway**:

* The subsequent component is a 90/10 beam splitter. Here's how it divides the light:
  * **90% Path**: The major fraction (90%) of the light goes through a diffractive filter array (DFA) and a 4f system. The terminal destination for this portion of the light is the Prophesee EVK3 event-based camera.
  * **10% Path**: The smaller fraction (10%) is channeled through a tube lens. This light is then focused onto the sensor of an amscope MU130 scientific CMOS camera.

***

### _Figures_

**Left to Right:** Transmittance graph for the optical components, Optical Setup Diagram

![](<../.gitbook/assets/image (1) (1) (1) (1).png>)![](<../.gitbook/assets/image (1) (1) (1).png>)

### Errata

* The beam expander pictured in the optical setup diagram is no longer a part of the setup.
