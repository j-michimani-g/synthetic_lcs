# synthetic lightcurves
A guide on how to use the <samp>lcgenerator</samp> program to create synthetic lightcurves.

The syntax to run the program in the Linux terminal is:
`````
cat lcs | lcgenerator [-v] input_par shape out_lcs
`````

where the input files needed are:
- lcs: input lightcurves 
- input_par: input parameters 
- shape: input shape

The **input lightcurves** file contains epochs and the corresponding geometry i.e. the JD epoch (light-time corrected), the brightness (not used in the <samp>lcgenerator</samp> routine) and the ecliptic asteroid-centric cartesian coordinates x, y, z of the Sun and of the Earth in AU.


The **input parameters** file contains the spin vector direction, period, and scattering parameters – the first line contains asteroid’s rotation parameters: ecliptic pole coordinates λ, β (deg), and the rotation period P (hours). The second line contains zero time t0 (JD) and the initial rotation angle φ0 (deg). Then phase function parameters (the third line) and the Lambertian part of the scattering model (the fourth line) follow.

The **input shape** file contains a polyhedral convex shape model with triangular surface facets. The format of the file is as follows: the first line gives the number of vertices and facets, then follow the vertex x, y, z coordinates, then for each facet the number of vertices and the order numbers of facet vertices
(anticlockwise seen from outside the body).


The **input lightcurves** file can be created using the notebook named XXXXX in this repository. Both the **input parameters** and **input shape** can be downloaded from the DAMIT database. 
