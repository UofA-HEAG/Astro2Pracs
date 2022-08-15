# Research Project: Gamma-Ray Observations and Modeling of Supernova Remnants

Topics: HESS, python programming, supernova remnants, diffusion, modeling, cosmic rays, gamma rays, interstellar medium.

## Motivation
Supernova Remnants (SNRs) are astrophysical objects, emitting radiation over the complete electromagnetic spectrum.
They are the remains of stars that exploded in a supernova, and their shock wave is expanding into the interstellar medium. 
SNRs are thought to be responsible for the acceleration of galactic cosmic rays.
They can produce energetic shock fronts with cosmic-ray particles of ultra-high energy, but it still remains a mystery if they are also able to accelerate cosmic rays up to PeV energies. 
Cosmic-ray protons can interact with the interstellar medium and produce gamma rays via pion decay. 
Therefore, gamma-ray observations can be used to study these intriguing objects.

Gamma-ray astronomy is a rather young research field and covers the study of the upper part of the electromagnetic spectrum (MeV to TeV energy regime). Depending on the targeted energy of the gamma rays, the measurement with satellite- or ground-based instruments is advantageous. High-energy (HE) gamma rays are typically measured with satellites, while very-high-energy (VHE) gamma rays are measured from the ground. Imaging Air Cherenkov Telescopes (IACTs) measure the Cherenkov light that is emitted by the extensive air shower, initiated by the gamma ray interacting with the Earth's atmosphere. The particles of this shower can also be detected using the water Cherenkov method.

This research project aims to model the cosmic rays and gamma rays from supernova remnants to reveal the origin of the unidentified gamma-ray source HESS J1804-216.


## Schedule
* Week 3 (August 8): Overleaf. Introduction.
* Week 4: Python / Modelling
* Week 5: Modelling
* Week 6: Plotting / Morphology
* Week 7: Morphology
* Week 8 (September 12): Structure your report, include figures and tables, write dot points. Discuss with Sabrina.
* Week 9 (October 3): Public holiday
* October 4: Submission of the group report (!)


## Tasks

* **Introduction**. Read up on the following keywords: Astroparticle physics, gamma-ray astronomy, HESS Galactic Plane Survey (HGPS), supernova remnants, diffusive transport/propagation. 
Think about the following questions: 
    - What is astroparticle physics? Which particles are studied in this field? What are the advantages and disadvantages of each of these particles?
    - What is gamma-ray astronomy? How can gamma rays be measured? What are the advantages and disadvantages of the different techniques? Which measurement is used in which energy regime? 
    - What is the HGPS? What are the source types and their number counts?
    - What are Supernova Remnants (SNRs)? How do they evolve with age? Through which phases do they go?
    - There are 2 basic scenarios regarding the accleration of cosmic rays in SNRs: Leptonic and hadronic. What processes are involved / possible to create gamma rays?
    
* **Modeling Cosmic-ray Protons**. Here and in the following we will only consider cosmic-ray protons from an impulsive accelerator. Implement different models for generating proton spectra (energy vs flux) by implementing a function (-> `def`) with `(E,R,t)` as input and `J(E,R,t)` as output. The basic equations come from http://articles.adsabs.harvard.edu/pdf/1996A%26A...309..917A. Assume that t << tau_pp. Model parameters should be free parameters and be added to your input. Use `astropy.units` in this task.

    1. Emission from SNR centre.
    2. Emission from SNR centre if t > escape time. An equation for the escape time can be found in https://ui.adsabs.harvard.edu/abs/2009MNRAS.396.1629G.
    3. Emission from shell with escape radius. An equation for the escape radius can be found in https://www.annualreviews.org/doi/abs/10.1146/annurev.astro.46.060407.145237.
    4. Emission from shell with escape radius if t > escape time.

* **Modeling Gamma Rays**. Based on a model of cosmic-ray protons, gamma rays can be modeled using https://journals.aps.org/prd/abstract/10.1103/PhysRevD.74.034018. Implement a function with the following inputs: proton model (previous task), volume and number density of a cloud, distance between cloud and Earth. 

* **Investigation of Cosmic-Ray Proton Models**. For every model, compare how different parameters influence the resulting spectrum. For example:
    - Age: 1, 10, 50 kyrs
    - Distance R to SNR centre: 10, 50, 150, 200, 250 pc
    - Diffusion parameters: chi 1, 0.1, 0.01, delta 0.3, 0.5, 0.7
    - Time development delta_p: 0.5, 1.5, 2.5
Moreover, compare the different models with similar parameters to each other. How do they differ?

* **Investigation of Gamma-Ray Models** For one model, compare how different parameters influence the resulting spectrum. For example:
    - nH: 100, 200, 300 1/cm^3
    - Distance Earth to cloud: 1, 5, 10 kpc
    - Distance SNR centre to cloud: 10, 50, 150, 200, 250 pc
    - Cloud extension: 50, 100 pc

* **Plotting in astropy**. In the following, we will investigate the unidentified gamma-ray source HESS J1804-216 from the HGPS. In previous studies, it was found that there are 2 promising candidates to be the accelerator of this source. Candidate 1: The SNR G8.7-0.1. Candidate 2: The progenitor SNR of the pulsar PSR 1803-2137. 
    - Download the flux map from the HGPS (https://www.mpi-hd.mpg.de/hfm/HESS/hgps/) and plot the region of interest with astropy.
    - Overlay the map with the positions of the 2 candidates and HESS J1804-216. For the pulsar, also mark the birth location (can be calculated by considering the proper motion and age, which can be found in the ATNF pulsar catalog).

* **Model morphology** A dedicated python code has been developed to use the above equations to model the morphology of protons and gamma rays in detail. Install and use this code to model HESS J1804-216 in detail. 
    - Ask Sabrina for the code, the gas maps and some settings to start with.
    - Run the code for different settings and compare to the HGPS observations to find the best match between model and observations.
What is the best candidate to be the origin of the unidentified gamma-ray source HESS J1804-216? What are the properties of the model?
