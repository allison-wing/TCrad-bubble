# TCrad-bubble
Model configuration files and post-processed output data files from bubble simulations of TC radiative feedbacks.
•	Each sub-folder contains model input files each set of simulations:
o	bubble_ctrl
o	bubble_lwqradfix
o	bubble_lwradqvfix
o	bubble_nocrf
o	bubble_nodiurnal
o	bubble_noqci
o	bubble_noqcl
o	bubble_qradfix
o	bubble_radhomo
o	bubble_radqvfix
o	bubble_swqradfix
o	bubble_swradqvfix

Model Input Files: For SAM6.11.2 (Khairoutdinov and Randall, 2003)
•	prm: namelist parameter file
•	snd: initial sounding
•	grd: vertical grid
•	qvprof: prescribed water vapor mixing ratio sounding (for bubble_radqvfix, bubble_lwradqvfix, bubble_swradqvfix)
•	rad: prescribed radiative heating rate profile (for bubble_qradfix, bubble_lwqradfix, bubbe_swqradfix)

Post-Processed Model Output Files:
•	urad.mat:
•	varbud.mat:
•	vtan.mat:
•	domainmeanvarbud/domainmeanvarbud_bubble_$simulation.mat: domain mean of terms in moist static energy variance budget
o	mean_$var = domain mean, hourly mean
o	dmean_$var = domain mean, daily mean
o	fmse = hourly mean column-integrated frozen moist static energy
o	fmsei = hourly instantaneous column-integrated frozen moist static energy
o	hadve = advective feedback, explicitly calculated
o	hadvr = advective feedback, as a residual
o	hhadve = horizontal component of advective feedback, explicitly calculated
o	hLW = longwave feedback
o	hLWc = clear-sky longwave feedback
o	hsef = surface flux feedback
o	hsefdk = disequlibrium component of surface flux feedback
o	hsefeddy = eddy component of surface flux feedback
o	hsefu = wind speed component of surface flux feedback
o	hSW = shortwave feedback
o	hSWc = clear-sky shortwave feedback
o	hvadve = vertical component of advecrtive feedback, explicitly calculated
o	tnfmsevar = tendency of FMSE variance
o	varh = FMSE variance

Other Post-Processed Model Output Files Available Upon Request:
For each simulation,
•	sfcwindspd.mat: wind speed at the lowest model level, as a function of x,y, and time. 
•	radaziwinds_az.mat: azimuthal mean tangential wind and azimuthal mean radial wind, as a function of z, radius from the TC center, and time. 
•	lwqrad_radazi.mat: azimuthal mean longwave radiative heating rate, as a function of z, radius from the TC center, and time.
•	RH_radazi.mat: azimuthal mean relative humidity, as a function of z, radius from TC center, and time.
•	NetRad_radazi.mat: azimuthal mean radiative fluxes, as a function of radius from the TC center and time. (net longwave at the surface (LWNS), net longwave at the TOA (LWNT), net shortwave at the surface (SWNS), net shortwave at the TOA (SWNT)).
•	NetRadCS_radazi.mat: Same as NetRad_radazi.mat but for clear-sky radiative fluxes.
