# windy-blr-2020
Data and scripts for Matthews et al. 2020 paper entitled "Stratified disc wind models for the AGN broad-line region: ultraviolet, optical and X-ray properties", [arXiv:2001.03625](https://arxiv.org/abs/2001.03625)

Please feel free to play around with the data or make your own plots. If you use this data or any of the code, please cite the MNRAS paper. 

See also: 

https://github.com/jhmatthews/quasar-wind-grid

https://github.com/agnwinds/python

## Data Structure
The data for every model is stored in folders for spectra (spectra/) and folders for physical conditions (physics/). The latter just contains the grid cells with their ionizing photon flux and hydrogen number density. The data are in astropy format and can be read in using the function astropy.io.ascii.read(). There are two jupyter notebooks describing how to read and plot the data in each case. 

Filenames have this style format: 
```
run52_thmin70_thmax85_rv1e19_f0p01_r1.spec
```

where the numbers refer to the run number, the minimum and maximum opening angles, the acceleration length, the clumping factor (f1=1,f0p1=0.1,f=0p01=0.01) and the launch radius in units of 450 r_g. 

### Spectra data files 

The header contains the parameters for the files, with comments denoted by hashes. The column headers are then 

```
Freq.  Lambda    Created  Emitted   CenSrc     Disk     Wind  HitSurf Scattered A05 A10 A15 [et cetera]
```

where Freq. and Lambda and frequency and wavelength and the other columns refer to various fluxes in the system. Fluxes at an angle 60 degrees are in the column A60. 

Important: All fluxes have units of flux in somewhat arbitrary units of erg/s/cm^2/Angstrom at 10 Gigaparsecs. This should be rescaled for any realistic quasar flux you desire. 


### Physical data files 

Data for the values of phi_H (units of number of photons cm^-2 s^-1), n_H (cm^-3) and lyman alpha emissivity (erg/s/cm^3) in each cell. 

```
x z var inwind i j
```

where x is the x coordinate of the cell in cm, z is the z coordinate in cm, var is the variable in question, inwind is whether the cell is completely in the wind (0), partly in the wind (1), not in the wind (-1) or a dummy/ghost cell (-2), and i and j are the indices of the cell. The inwind cell can be used to mask portions of the wind in plots.

## Questions or Ideas
email: matthews [at] ast.cam.ac.uk
or open a github issue! 
