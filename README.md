# windy-blr-2020
Data and scripts for Matthews et al. 2020 paper entitled "Stratified disc wind models for the AGN broad-line region: ultraviolet, optical and X-ray properties".

Please feel free to play around with the data or make your own plots. If you use this data or any of the code, please cite the MNRAS paper. 

See also: https://github.com/jhmatthews/quasar-wind-grid

### Data Structure
The data for every model is stored in folders for spectra (spectra/) and folders for physical conditions (physics/). The latter just contains the grid cells with their ionizing photon flux and hydrogen number density. The data are in astropy format and can be read in using the function astropy.io.ascii.read(). There are two jupyter notebooks describing how to read and plot the data in each case. 

### Questions or Ideas
email: matthews [at] ast.cam.ac.uk
