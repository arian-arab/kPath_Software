# kPath (Software to Simulate Angle-Resolved Photoelectron Spectroscopy Experiments-ARPES)

This package includes Python code and a MATLAB GUI that independently simulate ARPES measurements using Density Functional Theory (DFT) calculations.

As an example, DFT calculations for the material TaAs are provided. The reciprocal lattice units are defined, and the DFT results are stored in a NumPy array of size (51×51×51×22). Here, the three 51-dimensional components represent the x, y, and z components in the reciprocal space while the 22 corresponds to the number of bands, meaning that at each point in reciprocal space, the energies of 22 bands are computed.

In an ARPES experiment, using experimental parameters and geometry (such as photon energy, incidence angle, and sample orientation), a one-dimensional path in reciprocal space (k-path) can be defined. The corresponding energies for each of the 22 bands along this k-path can then be extracted. For instance, at a photon energy of 500 eV and an incidence angle of 90 degrees (assuming no contribution to the x component of electron energies from photon momentum), with an experimental setup of 0° tilt, 0° phi, and 0° theta, 22 line plots along the k-path can be obtained and are shown here:

<div align="center">
![Fig2](https://github.com/user-attachments/assets/15d23aa1-8d72-4f73-a392-270e3da334d0)
</div>

In the next step by rotating the sample along the y-axis (i.e. taking measurements by tilting the sample) we can obtain these bands along different k-path corresponding to different tilt values. Here as an example we rotate the sample by introducing tilt angles from -10 to 10 degress in steps of 0.1 degress:

![tilt_video](https://github.com/user-attachments/assets/d6c9cd29-b6e3-41f3-9ab1-581d974c0756)

All these 22 bands for each of the tils can be plotted in a 3-dimensional plot to better visualize the 22 bands along different k-paths:

![Fig1](https://github.com/user-attachments/assets/c1514d49-d6a3-4ea1-9bfd-6f837bf7a057)


The tilt in the above corresnpods to the k_y component. As a result by sclicing planes along the k_x-k_y direction we can obtain isoeneergetic surfaces hence resolve the ARPES image along the x and y components of the reciprocal space:

![isoenergy](https://github.com/user-attachments/assets/9e645fdb-af88-4c05-b536-dc56a92b022a)
