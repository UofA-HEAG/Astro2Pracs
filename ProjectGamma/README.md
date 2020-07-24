# Research Project: Gamma-Ray Observations of Active Galactic Nuclei

Topics: Fermi-LAT, CTA, statistics, python programming, Active Galactic Nuclei, Extragalactic Background Light

## Motivation
What's interesting about AGNs?
Gamma-ray astronomy. HE vs VHE. IACTs.
What is CTA?
CTA will work as open observatory. Like for most observatories / experiments, observation proposals have to be written for that. 
Therefore: Choose target and prepare everything you need for a proposal. Describe why they are interesting, how you picked them and what the detection prospects are. This is summarising the following work.

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
    - Plot the effective area vs energy for different sites, telescope types, zenith angles and pointing offsets. 

* **Estimation of required observation time**. How many hours are required to detect the source? How many hours are required to derive a spectrum with 3 energy bins and a binning of 5 bins per decade?

* **Visibility**. IACTs can only observe during night time. Depending on the location of the telescope, different parts of the sky are visible under different zenith angles.
    - You can derive the visibility of your source for different telescope locations here: http://tevcat.uchicago.edu/CustomVis.pl. For CTA-North, choose "MAGIC".
    - Which CTA site is better suited - CTA-North or CTA-South?
    - Show the visibility for your source for the year 2021.
    - Determine the time windows and zenith angles that are best suited to observe the proposed sources

* **Description of the proposed observations**. Based on the above, describe the observations you would request in a proposal.
    - CTA-North or CTA-South
    - Which telescopes?
    - Wobble offset configuration
    - Table with observation time windows and corresponding zenith angle
