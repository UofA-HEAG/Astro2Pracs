# Research Project: Observations with Adelaide's All-Sky Camera: Studies of the Atmosphere & Stars, Novae and other Transients

Topics: python programming, all-sky camera, analysis, atmosphere, stars, novae

## Motivation

Observations by any optical telescopes are affected by clouds and characteristics of the atmosphere. As these observations take place during nighttime, the identification of clouds in the sky is challenging and requires advanced devices and analysis techniques. One approach is to use all-sky camera images and a sophisticated software developed in Adelaide to determine the visibilities of stars and compare them to catalogue values. As clouds reduce the visibility of a star, this provides transmission (=cloudiness) measurements of the entire sky, together with cloud maps. Other usages of all-sky cameras include observations of serendipitous transients (short-lived events, such as novae), and brightnesses of stars over time (e.g. cepheids). Such all-sky camera is installed on the roof of the Oliphant building and has been taking data for more than a year.  

## Schedule
* Week 3: Overleaf. Introduction atmospheric monitoring, variable astronomical objects.


## Tasks

* **Introduction**. Read up on the following keywords: Atmospheric monitoring and devices, all-sky cameras and how to analyse their night-sky images, hipparcos star catalogue. Variable stars and astrophysical objects, novae. 
Think about the following questions: 
    - List different atmospheric conditions. How do atmospheric conditions influence astronomical images? What different devices / methods measure atmospheric conditions? What are their advantages / disadvantages? How can all-sky cameras be used to measure atmospheric conditions?
    - What type of variable astronomical objects are there? How can you get information about variability from star catalogues? What are novae? List the brightest novae of the past year that were visible from Australia (including their magnitude). How can all-sky cameras be used to measure astronomical objects and/or their variability?

* **All-Sky Camera**. You can check the latest camera captures and download images here: [http://allsky.physics.adelaide.edu.au](http://allsky.physics.adelaide.edu.au/). You will first need to connect to the university's VPN. Ask Sabrina for the username/password for the database.
  
* **quocca**. Install and familiarise with the all-sky camera software 'quocca'. (https://github.com/seinecke/quocca). There are different ways on how to set up and run it. Depending on your OS, experience etc, one might be easier than the other.
 - Using anaconda
 - Using Google Collab

* **Initial tasks**.
  - Check (physical) calibration: Mark the brightest stars in the image and check if they align with the visible stars
  - Check above for different days over the last year (it might need re-calibration)
  - Add labels with star names
  - Pick a variable bright star and a non-variable bright star. Determine their brightness over a) multiple hours in one night b) multiple days/weeks.
 
* **Tasks**
  Select different analysis time ranges, and assign one to each member of the group. For each of them:
  - Find a 'reference night', i.e. a clear night without clouds and minimum light pollution / moon
  - Calibrate the camera parameters and check calibration. Make a histogram of the distances between catalog position and fitted position (for large population of stars). Now make a 2d histogram with true magnitude vs above distance.
  - Estimate the point spread function (sigma)
  - Estimate the size of the crop around a star (fit_size)
  - Use the estimated sigma and fit_size in the settings of the detection methods (llh and filter) and compare the methods (e.g. by looking at the 2D histogram of true vs fitted magnitude)
  - Calibrate the fitted magnitude to correspond to the star's magnitude.
  - Add calibration line to above 2D histogram.
Pick a) a bright variable star (i.e. cepheid) and b) a bright astronomical transient (e.g. nova). For each:
- Determine the fitted magnitude with at least one image per night over your entire analysis period.
- Combine results with other group members.
- Discuss the derived light curves (time vs magnitude).
