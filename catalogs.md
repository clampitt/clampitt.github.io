<div class="container">

[Home](index.html) /
[Research](research.html) / 
**Catalogs** /
[Curriculum Vitae](cvitae.html) / 
[Publications](publications.html) /
[Blog](blog.html)

***

# SDSS Void Catalog

This void catalog uses a novel algorithm to look for voids in 2D slices of the galaxy distribution.
Individual slices are then combined to create the final, 3D void catalog.
This catalog enabled the first $5\sigma$ detections of void lensing ([Clampitt and Jain 2015](http://adsabs.harvard.edu/abs/2015MNRAS.454.3357C)) and void autocorrelations ([Clampitt, Jain, and Sanchez 2016](http://adsabs.harvard.edu/abs/2016MNRAS.456.4425C)).
The galaxy sample used to define these voids is the DR7 Luminous Red Galaxy sample of [Kazin et al. (2010)](http://adsabs.harvard.edu/abs/2010ApJ...710.1444K).
If you use this void catalog, please cite this paper which describes the algorithm:\
Clampitt, J., & Jain, B. 2015, MNRAS, 454, 3357

<a href="voids_clampitt-jain_SDSS_lrg-tracers.fit" download>Download Void Catalog</a>

### Catalog contents

Column        Meaning                                                    Units
-----------   -------------------------------------                      ----------
    ra        Void center (angular position)                             degrees
    dec       Void center (angular position)                             degrees
     z        Void center (redshift position)                               -
   r_los       void center (redshift position)                           comoving Mpc/h
    R_v        radius projected on the sky                                comoving Mpc/h
  theta_v      radius projected on the sky                                arcminutes
 los_size      void size in the line-of-sight direction                   comoving Mpc/h
 dens_rand     random point density                                       (degrees)$^{-2}$
   f_vol       Volume overlap fraction with a larger neighbor              -

### Important cuts

1. Require (dens_rand > 100) to remove voids near the survey edges.

2. In published papers I've always required the ratio of transverse to line-of-sight sizes to be within a factor of three:
*(1/3 $\leq$ R_v / los_size) AND (R_v / los_size $\leq$ 3)*.
This cut removes long, pencil-shaped objects and flat, pancaked-shaped objects.
These objects are more likely due to Poisson noise in the galaxy sampling rather than actual cosmic voids.

In principle you could explore other cuts on dens_rand and void axis ratio.
[Clampitt and Jain (2015)](http://adsabs.harvard.edu/abs/2015MNRAS.454.3357C)
describes the motivations for these particular cuts.


### Random catalogs

The random catalogs for different cuts on void size and volume overlap are available below.
The void size cuts are based on an effective radius that combines transverse and line-of-sight void sizes:

$r_{eff}$ = ($R_v^2 \times$ los_size)$^{1/3}$

Make the same cuts on the void catalog (for both $r_{eff}$ and $f_{vol}$) and use the corresponding random catalog.
Also be sure to do cuts 1 and 2 above (under "Important cuts") since these have also been applied to the random catalogs.

<a href="random-voids_clampitt-jain_reff15-20_fvol50.fit" download>Download Random Catalog</a>
(15 Mpc$/h < r_{eff} < 20$ Mpc$/h$) AND ($f_{vol} < 0.50$)\
<a href="random-voids_clampitt-jain_reff20-25_fvol50.fit" download>Download Random Catalog</a>
(20 Mpc$/h < r_{eff} < 25$ Mpc$/h$) AND ($f_{vol} < 0.50$)\
<a href="random-voids_clampitt-jain_reff25-30_fvol50.fit" download>Download Random Catalog</a>
(25 Mpc$/h < r_{eff} < 30$ Mpc$/h$) AND ($f_{vol} < 0.50$)

<a href="random-voids_clampitt-jain_reff15-20_fvol90.fit" download>Download Random Catalog</a>
(15 Mpc$/h < r_{eff} < 20$ Mpc$/h$) AND ($f_{vol} < 0.90$)\
<a href="random-voids_clampitt-jain_reff20-25_fvol90.fit" download>Download Random Catalog</a>
(20 Mpc$/h < r_{eff} < 25$ Mpc$/h$) AND ($f_{vol} < 0.90$)\
<a href="random-voids_clampitt-jain_reff25-30_fvol90.fit" download>Download Random Catalog</a>
(25 Mpc$/h < r_{eff} < 30$ Mpc$/h$) AND ($f_{vol} < 0.90$)

Also note:

1. The redshift distribution of smaller voids does not match the randoms perfectly.
If your measurement is very sensitive to the redshift, then the randoms for voids with reff < 25 may not be good enough.

2. There are at least 10 times as many randoms as voids for each sample.
But for some samples there are as many as 20 times as many randoms as voids.
So to use all voids with $r_{eff}$ = 15-30 Mpc$/h$ do not just append the random catalogs together.
You must take the same proportion of random points from each subsample.

3. As of May 12, 2017 I replaced the void catalog download link.
The only difference is the recent version removes two small, disconnected patches with a few hundred voids.
This ensures the geometry of the void catalog matches the random catalogs.


</div>