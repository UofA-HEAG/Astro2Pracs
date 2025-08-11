# Research Project: Gamma-Ray Observations of Active Galactic Nuclei

Topics: Fermi-LAT, CTAO, statistics, python programming, Active Galactic Nuclei, Extragalactic Background Light

## Motivation

Active Galactic Nuclei (AGN) are astrophysical objects, emitting radiation over the complete electromagnetic spectrum. A supermassive black hole in the centre of a galaxy is accreting matter from its surroundings, the accretion disc, and the main power source of an AGN. Above the disc, the broad line region can be found, producing broad emission lines in the optical and ultraviolet range. A dust tours sourrounds the accretion disc, obscuring often the inner part of the AGN depending on the viewing angle. Beyond the broad line region, there is the narrow line region, which emits narrow emission and absorption lines. Depending on the accretion rate, two strongly collimated relativistic jets, perpendicular to the accretion disc, can be produced.
Different wavebands provide different windows to AGN physics: The infrared band is mostly sensitive to obscuring material and dust, the optical/ultraviolet band is connected to the emission from the accretion disc, and the X-ray band traces the emission of a corona. In the radio and gamma-ray band strong non-thermal radiation is emitted, related to the jet.

Gamma-ray astronomy is a rather young research field and covers the study of the upper part of the electromagnetic spectrum (MeV to TeV energy regime). Depending on the targeted energy of the gamma rays, the measurement with satellite- or ground-based instruments is advantageous. High-energy (HE) gamma rays are typically measured with satellites, while very-high-energy (VHE) gamma rays are measured from the ground. Imaging Air Cherenkov Telescopes (IACTs) measure the Cherenkov light that is emitted by the extensive air shower, initiated by the gamma ray interacting with the Earth's atmosphere. The particles of this shower can also be detected using the water Cherenkov method.

The Cherenkov Telescope Array Observatory (CTAO) is the next-generation observatory for ground-based gamma-ray astronomy. With more than 100 telescopes equipped with state-of-the-art technologies, it will achieve unprecedented sensitivity and angular resolution, providing a new view of the sky at energies from 20 GeV to more than 300 TeV.

CTAO will be operated as a proposal-driven open observatory. This means that every observation has to be requested and an observation proposal has to be written. Therefore, this research project focuses on the necessary steps to develop such a proposal. 


## Schedule
* Week 3: Overleaf. Introduction gamma-ray astronomy.
* Week 4: Python
* Week 5: Tasks
* Week 6: Tasks
* Week 7: Tasks
* Week 8: Tasks
* Week 9: Structure your report, include figures and tables, write dot points. Discuss with Sabrina.


## Tasks

* **Introduction**. Read up on the following keywords: Astroparticle physics, gamma-ray astronomy, imaging air cherenkov telescopes, Cherenkov Telescope Array, Fermi-LAT, Active Galactic Nuclei, extragalactic background light. 
Think about the following questions: 
    - What is astroparticle physics? Which particles are studied in this field? What are the advantages and disadvantages of each of these particles?
    - What is gamma-ray astronomy? How can gamma rays be measured? What are the advantages and disadvantages of the different techniques? Which measurement is used in which energy regime? 
    - What are Active Galactic Nuclei (AGN)? Which subtypes of AGN exist and how are they distinguished?
    - What is the extragalactic background light? How does this light influence gamma rays and the gamma-ray spectrum measured at Earth?
    
* **Selection of the AGNs to be observed.** Select ~10 AGNs (blazars) from the Fermi-LAT catalogue, covering a redshift range of z=0...1. Consider the flux normalisation and spectral shape to pick sources that are likely to be detected in VHE. In case of FSRQs with z>0.8, assume that they are in a flaring state where the flux is 5 times the average flux.
    - A catalogue of sources detected in HE (Fermi-LAT) can be found here: [https://fermi.gsfc.nasa.gov/ssc/data/access/lat/12yr_catalog/](https://heasarc.gsfc.nasa.gov/w3browse/fermi/fermilpsc.html).
    - A catalogue of AGNs detected with Fermi-LAT: https://heasarc.gsfc.nasa.gov/w3browse/fermi/fermilac.html
    - A catalogue of blazars including redshifts: https://heasarc.gsfc.nasa.gov/w3browse/all/romabzcat.html

* **Fermi-LAT spectrum**. Based on the above catalogue(s), plot the spectral function and data points with uncertainties. Think about how to illustrate uncertainties and where to plot uncertainty bars. Calculate the uncertainty region of the spectral function (it will create a "butterfly").

* **Estimation of the VHE spectrum based on the HE spectrum**. Gamma rays travelling through the Universe interact with the extragalactic background light (EBL) and will be absorbed. This means that the spectrum measured at Earth is different from the intrinsic spectrum at the source. To estimate the spectrum in VHE, the spectrum in HE can be extrapolated and corrected for the EBL.
    - Information about the EBL can be found here: https://www.sciencedirect.com/science/article/pii/S0927650512001740?via%3Dihub
    - gammapy has a model 'EBLAbsorptionNormSpectralModel' that allows to select different EBl models and different alpha normalisation values

* **Simulation of a CTAO measurement**. The python package gammapy allows a simulation of how many events would be measured by a specific telescope configuration (CTA site, telescope types) under specific observational conditions (zenith angle, pointing offset) in a given time for a specific spectrum. 
    - An example can be found here: [https://docs.gammapy.org/1.2/tutorials/analysis-1d/spectrum_simulation.html]
    - Include the EBL absorption in your spectral model. Pick one of the available models and a scaling factor (but don't tell the 'analysis' task force - it's their task to recover this information).
 
* **Analysis of the simulated CTAO measurement**. Gammapy also allows an analysis of the simulated dataset.
    - An example can be found here (ignore the first part and ignore the loop over datasets of the same observation): [https://docs.gammapy.org/1.2/tutorials/analysis-1d/spectrum_simulation.html]
    - Plot the spectrum (absorbed and deabsorbed) for each AGN.
    - Fit the spectrum (check which model and scaling factor gives the best result) for each AGN
    - Which EBL model and which scaling factor was used, based on the results for all AGNs together?

* **Estimation of required observation time and zenith angle**. How many hours (for each AGN separately) are required to recover the EBL model? How do the results change dependent on observation time? Which zenith angle is best to recover the EBL model? How do the results change dependent on zenith angle?

* **Visibility**. IACTs can only observe during night time. Depending on the location of the telescope, different parts of the sky are visible under different zenith angles.
    - You can derive the visibility of your source for different telescope locations here: http://tevcat.uchicago.edu/CustomVis.pl. For CTA-North, choose "MAGIC".
    - Which CTA site is better suited for each AGN - CTA-North or CTA-South?
    - Show the visibilities for one example source for the year 2025.
    - Determine the time windows and zenith angles that are best suited to observe the proposed sources

* **Description of the proposed observations**. Based on the above, describe the observations you would request in a proposal.
    - CTA-North or CTA-South
    - Table with observation time windows and corresponding zenith angle
 
  
