# source_id_to_orbits
This repo turns source_id's (Gaia DR2 or EDR3) into posteriors on the total orbit velocity and integrates the orbit of the star round the Galaxy.

Enter the Gaia DR2 or EDR3 source_id's of the stars you are interested in in candidates.dat. If you know their radial velocity then also put that in there, otherwise either 
1) enter radial_velocity = 0 and radial_velocity_error = -9999 to use the global radial velocity prior you set in the notebook
  or
2) enter the mean and standard deviation of the radial velocity prior you would like to use for this specific star.
  
The notebook will then step you through:
1) Downloading the rest of the data from the Gaia archive.
2) Correcting for the parallax zeropoint.
3) Sampling within the uncertainties.
4) Integrating orbits using gala.
5) Plotting orbits and posteriors on the total galactocentric velocity.
