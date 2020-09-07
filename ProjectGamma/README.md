# Research Project: Gamma-Ray Observations of Active Galactic Nuclei

Topics: Fermi-LAT, CTA, statistics, python programming, Active Galactic Nuclei, Extragalactic Background Light

## Motivation

Active Galactic Nuclei (AGN) are astrophysical objects, emitting radiation over the complete electromagnetic spectrum. A supermassive black hole in the centre of a galaxy is accreting matter from its surroundings, the accretion disc, and the main power source of an AGN. Above the disc, the broad line region can be found, producing broad emission lines in the optical and ultraviolet range. A dust tours sourrounds the accretion disc, obscuring often the inner part of the AGN depending on the viewing angle. Beyond the broad line region, there is the narrow line region, which emits narrow emission and absorption lines. Depending on the accretion rate, two strongly collimated relativistic jets, perpendicular to the accretion disc, can be produced.
Different wavebands provide different windows to AGN physics: The infrared band is mostly sensitive to obscuring material and dust, the optical/ultraviolet band is connected to the emission from the accretion disc, and the X-ray band traces the emission of a corona. In the radio and gamma-ray band strong non-thermal radiation is emitted, related to the jet.

Gamma-ray astronomy is a rather young research field and covers the study of the upper part of the electromagnetic spectrum (MeV to TeV energy regime). Depending on the targeted energy of the gamma rays, the measurement with satellite- or ground-based instruments is advantageous. High-energy (HE) gamma rays are typically measured with satellites, while very-high-energy (VHE) gamma rays are measured from the ground. Imaging Air Cherenkov Telescopes (IACTs) measure the Cherenkov light that is emitted by the extensive air shower, initiated by the gamma ray interacting with the Earth's atmosphere. The particles of this shower can also be detected using the water Cherenkov method.

The Cherenkov Telescope Array (CTA) is the next-generation observatory for ground-based gamma-ray astronomy. With more than 100 telescopes equipped with state-of-the-art technologies, it will achieve unprecedented sensitivity and angular resolution, providing a new view of the sky at energies from 20 GeV to more than 300 TeV.

CTA will be operated as a proposal-driven open observatory. This means that every observation has to be requested and an observation proposal has to be written. Therefore, this research project focuses on the necessary steps to develop such a proposal. 


## Schedule
* Week 3 (August 10): Overleaf. Introduction gamma-ray astronomy.
* Week 4: Python
* Week 5: Tasks
* Week 6: Tasks
* Week 7: Tasks
* Week 8 (September 14): Structure your report, include figures and tables, write dot points. Discuss with Sabrina.
* Week 9 (October 5): Public holiday
* October 9: Submission of the group report (!)


## Tasks

* **Introduction**. Read up on the following keywords: Astroparticle physics, gamma-ray astronomy, imaging air cherenkov telescopes, Cherenkov Telescope Array, Fermi-LAT, Active Galactic Nuclei, extragalactic background light. 
Think about the following questions: 
    - What is astroparticle physics? Which particles are studied in this field? What are the advantages and disadvantages of each of these particles?
    - What is gamma-ray astronomy? How can gamma rays be measured? What are the advantages and disadvantages of the different techniques? Which measurement is used in which energy regime? 
    - What are Active Galactic Nuclei (AGN)? Which subtypes of AGN exist and how are they distinguished?
    - What is the extragalactic background light? How does this light influence gamma rays and the gamma-ray spectrum measured at Earth?
    
* **Selection of the AGN to be observed.** Select 2 AGNs: 1. One that has already been studied with IACTs. 2. One that has not been detected with IACTs, but with Fermi-LAT.
    - A catalog of sources detected in VHE can be found here: http://tevcat.uchicago.edu. If you click on a source, it will give you more information including publications about the source.
    - A catalog of sources detected in HE (Fermi-LAT) can be found here: https://fermi.gsfc.nasa.gov/ssc/data/access/lat/8yr_catalog/. Fermi-LAT is a gamma-ray telescope on a satellite. Make sure, that the redshift of your source is known. So far, sources up to redshifts of 0.9 could have been detected in the VHE range.

* **Literature review of the selected AGN.** 
    - Publications
    - VHE data
    - Multiwavelength data

* **Fermi-LAT spectrum**. Based on the above catalog, plot the spectral function and data points with uncertainties. Think about how to illustrate uncertainties and where to plot uncertainty bars. Calculate the uncertainty region of the spectral function (it will create a "butterfly").

* **Multi-wavelength spectral energy distributions**. Plot a spectral energy distribution (SED).
    - A SED builder tool can be found here: https://tools.ssdc.asi.it/cas/login?gateway=true&service=https%3A%2F%2Ftools.ssdc.asi.it%2FSED%2F. It shows you the SED, but you can also use it to download the data.
    - If sufficient data is available, plot the SED for different time ranges, for example for times of a flare.

* **Estimation of the VHE spectrum based on the HE spectrum**. Gamma rays travelling through the Universe interact with the extragalactic background light (EBL) and will be absorbed. This means that the spectrum measured at Earth is different from the intrinsic spectrum at the source. To estimate the spectrum in VHE, the spectrum in HE can be extrapolated and corrected for the EBL.
    - Information about the EBL can be found here: https://www.sciencedirect.com/science/article/pii/S0927650512001740?via%3Dihub
    - Ask Sabrina for data of the optical depth for the redshift of your source

* **Simulation of a CTA measurement**. The python package gammapy allows a simulation of how many events would be measured by a specific telescope configuration (CTA site, telescope types) under specific observational conditions (zenith angle, pointing offset) in a given time for a specific spectrum. 
    - An example can be found here: https://docs.gammapy.org/0.17/notebooks/spectrum_simulation.html
    - Plot the effective area vs energy for different sites, zenith angles and pointing offsets (North/South site, 20/40 deg zenith). 

* **Estimation of required observation time**. How many hours are required to detect the source? How many hours are required to derive a spectrum with 3 energy bins and a binning of 3 bins per decade?
    - Use Non, Noff from the previous task
    - To calculate a significance, consider the following paper: http://articles.adsabs.harvard.edu/pdf/1983ApJ...272..317L
    - Calculate both, equation (17) and Nexcess / sqrt(Noff)
    - To get a rough estimate of the observation time, you can scale the counts with the observation time. Once you have this estimate, run the simulation (previous task) again.

* **Visibility**. IACTs can only observe during night time. Depending on the location of the telescope, different parts of the sky are visible under different zenith angles.
    - You can derive the visibility of your source for different telescope locations here: http://tevcat.uchicago.edu/CustomVis.pl. For CTA-North, choose "MAGIC".
    - Which CTA site is better suited - CTA-North or CTA-South?
    - Show the visibility for your source for the year 2021.
    - Determine the time windows and zenith angles that are best suited to observe the proposed sources

* **Description of the proposed observations**. Based on the above, describe the observations you would request in a proposal.
    - CTA-North or CTA-South
    - Wobble offset configuration
    - Table with observation time windows and corresponding zenith angle
