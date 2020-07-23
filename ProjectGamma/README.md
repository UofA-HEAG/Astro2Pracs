# Research Project: Gamma-Ray Observations of Active Galactic Nuclei

Topics: Fermi-LAT, CTA, statistics, python programming, (machine learning)

## Motivation
Proposal

## Schedule
* Week 3 (August 10): Intro Gamma. Literature review. Get familiar with overleaf?
* Week 4: python
* Week 5: tasks
* Week 6: tasks
* Week 7: tasks
* Week 8 (September 14): Discuss remaining tasks within group. Get familiar with overleaf? Structure report. Discuss with Sabrina
* Week 9 (October 5): Public holiday
* October 9: Submission of the group report (!)


## Tasks

*	Write a proposal for CTA observations: Pick one or several sources. Describe why they are interesting, how you picked them and what the detection prospects are. This is summarising the following work. (Scientific writing, research, literature review)
Search for specific source types in the Fermi catalog: Set up a machine learning classification method (eg Random Forest) to classify different source types. Train on associated sources, apply to unassociated sources. Use 3FHL or 4FGL Fermi catalog. (Machine learning, working with Fermi catalog)
Search for unusual source types in the Fermi catalog: Set up a machine learning clustering method (eg Gaussian Mixture Model) to find unusual and hopefully interesting sources. (Machine learning, dimension reduction, working with Fermi catalog)
Literature review: Search astronomical databases (TeVcat, NED, ASDC) to find information about the found promising sources. (Different astronomical databases)
Summary of different observations: Obtain the CTA skymap (with gammapy) and overlay it with the source positions from the Fermi catalog and possibly further MWL data. Derive the SED by plotting the collected data and checking the SEDbuilder tool from ASDC. (Plotting, gammapy, CTA data, SED builder tool, astronomical databases)
VHE gamma-ray spectra with Gammapy: Pick a source from one of the simulated CTA surveys (I can provide them on a USB stick) and derive the spectrum. (Plotting, gammapy, CTA data)
HE gamma-ray spectrum: Pick a source, find it in Fermi (3FGL or 3FHL) catalog and plot the given spectrum. Plot both spectrum and data points with uncertainties. Think about how to illustrate uncertainties and where to plot uncertainty bars. (Plotting, uncertainties, working with Fermi catalog)
HE uncertainty region: Calculate the uncertainty region from the values given in the Fermi catalog (it will create a "butterfly") and plot it. (Plotting, error propagation, working with Fermi catalog)
Estimation of VHE spectrum: Extrapolate HE spectrum to VHE, absorb EBL and plot it. I can provide a file with absorption values for different energies and redshifts. This should be interpolated. (Programming, interpolation, EBL)
Estimation of observation prospects: Calculate the number of events we expect to observe for a given observation time. Compare to (different) CTA sensitivity curves and determine which
12/8/19, 12(39 pm
          about:blank Page 1 of 2

subarrays you need and how much observation time and which zenith regime. (Plotting, significance formula, integrals)
Estimation of neutrinos: Calculate how many neutrinos you would expect from the source for very basic assumptions for the IceCube detector (I have to write down the assumptions). (Neutrino astronomy, particle physics, integrals)
Observability: Check the observability of your source (e.g. with TeVCat). Under which zenith angle can it be observed for how many hours and during what time of the year. Come up with a list of observation times to cover your proposed observation time. (TeVcat tools)
Derivation of Li&Ma: I have a description on how to approach the formula step by step. (Likelihood-ratio test, Wilks theorem, probability distributions, meaning of significance) Long-term light curves: Obtain long-term light curves (possibly in different energy ranges) from Fermi-LAT and/or FACT. (Getting Fermi data)
Correlation of light curves: Study the correlation between different energy ranges. Determination of different sources phases: Apply the Bayesian block analysis to the light curves. (Programming, Bayesian statistics)
Simulation of ground-based detector: I have a description of the different simulation steps - source distribution, absorption, detection probability, measurement. Data could be further used for machine learning classification / regression and deconvolution. (Programming, simulation, rejection sampling, inverse transform sampling)
Deconvolution of gamma-ray spectra: Implement a very basic deconvolution method (or multiple ones to show the problems). Own simulated data or data from CTA/FACT could be used, but I have to check what is publicly available. (Programming, deconvolution, inverse / ill- posed problems)
12/8/19, 12(39 pm
        about:blank Page 2 of 2
