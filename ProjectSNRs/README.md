# Research Project: Gamma-Ray Observations and Modelling of Supernova Remnants

Topics: HESS, python programming, supernova remnants, diffusion, modelling, cosmic rays, gamma rays, interstellar medium.

## Motivation
Supernova Remnants (SNRs) are astrophysical objects, emitting radiation over the complete electromagnetic spectrum.
They are the remains of stars that exploded in a supernova, and their shock wave is expanding into the interstellar medium. 
SNRs are thought to be responsible for the acceleration of Galactic cosmic rays.
They can produce energetic shock fronts with cosmic-ray particles of ultra-high energy, but it still remains a mystery if they are also able to accelerate cosmic rays up to PeV energies. 
Cosmic-ray protons can interact with the interstellar medium and produce gamma rays via pion decay. 
Therefore, gamma-ray observations can be used to study these intriguing objects.

Gamma-ray astronomy is a rather young research field and covers the study of the upper part of the electromagnetic spectrum (MeV to TeV energy regime). Depending on the targeted energy of the gamma rays, the measurement with satellite- or ground-based instruments is advantageous. High-energy (HE) gamma rays are typically measured with satellites, while very-high-energy (VHE) gamma rays are measured from the ground. Imaging Air Cherenkov Telescopes (IACTs) measure the Cherenkov light that is emitted by the extensive air shower, initiated by the gamma ray interacting with the Earth's atmosphere. The particles of this shower can also be detected using the water Cherenkov method.

This research project aims to model the cosmic rays and gamma rays from a supernova remnant to reveal its origin.


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
    
* **Modelling Cosmic-ray Protons**. Here and in the following we will only consider cosmic-ray protons from an impulsive accelerator. Develop different models for generating proton spectra (energy vs flux). The basic equations come from http://articles.adsabs.harvard.edu/pdf/1996A%26A...309..917A. Assume that t << tau_pp.

    1. Emission from SNR centre.
    2. Emission from SNR centre if t > escape time. An equation for the escape time can be found in https://ui.adsabs.harvard.edu/abs/2009MNRAS.396.1629G.
    3. Emission from shell with shock radius. An equation for the shock radius can be found in https://www.annualreviews.org/doi/abs/10.1146/annurev.astro.46.060407.145237. You can use tsedov=1600yr. 
    4. Emission from shell with time-dependent escape radius (shock radius at escape time).

* **Investigation of Cosmic-Ray Proton Models**. For every model, compare how different parameters influence the resulting spectrum. Use partISM for this. For example:
    - Age: 1, 10, 50 kyrs
    - Distance R to SNR centre: 10, 50, 150, 200, 250 pc
    - Diffusion parameters: D0 1e27, 1e28, delta 0.3, 0.5, 0.7
    - Time development delta_p: 0.5, 1.5, 2.5
Moreover, compare the different models with similar parameters to each other. How do they differ?

* **Investigation of one or more Supernova Remnants**. Consider the following SNRs: HESS J1804-216, W28 and RX J1713.7-3946.
HESS J1804-216 is an unidentified gamma-ray source. In previous studies, it was found that there are 2 promising candidates to be the accelerator of this source. Candidate 1: The SNR G8.7-0.1. Candidate 2: The progenitor SNR of the pulsar PSR 1803-2137.
W28 is an old SNR and a prime candidate to study cosmic-ray diffusion, as the adjacent molecular clouds provide target material for gamma-ray production and due to its age, most particles escaped the shock front into the interstellar medium.
RX J1713.7-3946 is a young SNR and a prime candidate to search for escaping cosmic rays with PeV energies, as only the most energetic particles had a chance to escape in such a short time frame (given the young age).
  
* **Plotting in astropy**. In the following, investigate one or more of the above SNRs.
    - Download the flux map from the HGPS (https://www.mpi-hd.mpg.de/hfm/HESS/hgps/) and plot the region of interest with astropy.
    - Overlay the map with important information obtained from other observations. For example, in case of HESS J1804-216, the positions of the 2 candidates and HESS J1804-216. For the pulsar, also mark the birth location (can be calculated by considering the proper motion and age, which can be found in the ATNF pulsar catalog). In case of W28 and RX J1713, plot the current extension of the SNR as a circle. 

* **Model morphology** A dedicated python code has been developed to use the above equations to model the morphology of protons and gamma rays in detail. Install and use this code to model the chosen SNR(s) in detail. 
    - Ask Sabrina for the code, the gas maps and some settings to start with.
    - Run the code for different settings and compare to the HGPS observations to find the best match between model and observations.
HESS J1804-216: What is the best candidate to be the origin of the unidentified gamma-ray source HESS J1804-216? What are the properties of the model?
W28: Can you find a model matching the gamma-ray emission at different locations around the SNR? What are the properties?
RX J1713-3946: Matching the gamma-ray observations of the supernova remnant itself, how much gamma-ray emission can we expect from the adjacent clouds?

* **Investigation of Gamma-Ray Models** For one model, compare how different parameters influence the resulting spectrum. For example:
    - nH: 100, 200, 300 1/cm^3
    - Distance Earth to cloud: 1, 5, 10 kpc
    - Distance SNR centre to cloud: 10, 50, 150, 200, 250 pc
    - Cloud extension: 50, 100 pc
