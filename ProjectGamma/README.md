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
    
* **Science Question**. Discuss in the group the science question you want to investigate.
  - Have a look at the CTAO Science book for some ideas: https://arxiv.org/pdf/1709.07997
  - This group project will involve a simulation of the science question of interest. The following types of simulations are possible with gammapy: a) Simulation of an energy spectrum (energy vs flux). b) Simulation of a light curve (time vs flux) / simulation of a time-dependent energy spectrum (energy vs flux for different times). c) Simulation of a map (RA/DEC vs flux).
  - Have a look through the tutorials to get an idea what kind of things can be done and how they look: https://docs.gammapy.org/1.3/tutorials/index.html
Don't worry, the amount of information can look a bit overwhelming, but I will help you with coming up with more specific tasks and some gammapy examples once we have decided a direction.

* **naima**. Familiarise yourself with the software package naima (for modelling energy spectra).
  - https://naima.readthedocs.io/en/latest/
  - Install via '!pip install naima' (similar to gammapy)
  - Further information and examples under https://github.com/seinecke/anita23/blob/main/lectures/se-lectures.pdf and https://github.com/seinecke/anita23/blob/main/naima/naima_models.ipynb
 
* **gammapy**. There are different ways on how to set up and run gammapy. Depending on your OS, experience etc, one might be easier than the other.
    - Using anaconda: https://docs.gammapy.org/1.3/getting-started/index.html
    - Using Google Collab: See collab-gammapy.ipnb
Familiarise yourself with simulating 1D spectra: https://docs.gammapy.org/1.3/tutorials/analysis-1d/spectrum_simulation.html#sphx-glr-tutorials-analysis-1d-spectrum-simulation-py
  
