# TCrad-bubble
Model configuration files and post-processed output data files from Wing (2021) bubble simulations of TC radiative feedbacks.

Each sub-folder contains model input files for each set of simulations:

- bubble_ctrl
- bubble_lwqradfix
- bubble_lwradqvfix
- bubble_nocrf
- bubble_nodiurnal
- bubble_noqci
- bubble_noqcl
- bubble_qradfix
- bubble_radhomo
- bubble_radqvfix
- bubble_swqradfix
- bubble_swradqvfix

Model Input Files: For SAM6.11.2 (Khairoutdinov and Randall, 2003)

-	prm: namelist parameter file
-	snd: initial sounding
-	grd: vertical grid
-	qvprof: prescribed water vapor mixing ratio sounding (for bubble_radqvfix, bubble_lwradqvfix, bubble_swradqvfix)
-	rad: prescribed radiative heating rate profile (for bubble_qradfix, bubble_lwqradfix, bubbe_swqradfix)

Post-Processed Model Output Files:

-	urad.mat:
-	varbud.mat:
-	vtan.mat:
-	domainmeanvarbud/domainmeanvarbud_bubble_$simulation.mat: domain mean of terms in moist static energy variance budget
    -	mean_$var = domain mean, hourly mean
    -	dmean_$var = domain mean, daily mean
    -	fmse = hourly mean column-integrated frozen moist static energy
    -	fmsei = hourly instantaneous column-integrated frozen moist static energy
    -	hadve = advective feedback, explicitly calculated
    -	hadvr = advective feedback, as a residual
    -	hhadve = horizontal component of advective feedback, explicitly calculated
    -	hLW = longwave feedback
    -	hLWc = clear-sky longwave feedback
    -	hsef = surface flux feedback
    -	hsefdk = disequlibrium component of surface flux feedback
    -	hsefeddy = eddy component of surface flux feedback
    -	hsefu = wind speed component of surface flux feedback
    -	hSW = shortwave feedback
    -	hSWc = clear-sky shortwave feedback
    -	hvadve = vertical component of advecrtive feedback, explicitly calculated
    -	tnfmsevar = tendency of FMSE variance
    -	varh = FMSE variance

Other Post-Processed Model Output Files Available Upon Request:

For each simulation,
-	sfcwindspd.mat: wind speed at the lowest model level, as a function of x,y, and time. 
-	radaziwinds_az.mat: azimuthal mean tangential wind and azimuthal mean radial wind, as a function of z, radius from the TC center, and time. 
-	lwqrad_radazi.mat: azimuthal mean longwave radiative heating rate, as a function of z, radius from the TC center, and time.
-	RH_radazi.mat: azimuthal mean relative humidity, as a function of z, radius from TC center, and time.
-	NetRad_radazi.mat: azimuthal mean radiative fluxes, as a function of radius from the TC center and time. (net longwave at the surface (LWNS), net longwave at the TOA (LWNT), net shortwave at the surface (SWNS), net shortwave at the TOA (SWNT)).
-	NetRadCS_radazi.mat: Same as NetRad_radazi.mat but for clear-sky radiative fluxes.
