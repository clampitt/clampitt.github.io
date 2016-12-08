<div class="container">

[Home](index.html) /
[Research](research.html) / 
**Catalogs** /
[Curriculum Vitae](cvitae.html) / 
[Publications](publications.html) /
[Blog](blog.html)

***

## SDSS Void Catalog

The void catalog of [Clampitt and Jain (2015)](http://adsabs.harvard.edu/abs/2015MNRAS.454.3357C) uses a novel algorithm that looks for voids in 2D slices of the galaxy distribution.
Individual slices are then combined to create the final, 3D void catalog.
This catalog enabled the first $5\sigma$ detections of void lensing ([Clampitt and Jain 2015](http://adsabs.harvard.edu/abs/2015MNRAS.454.3357C)) and void autocorrelations ([Clampitt, Jain, and Sanchez 2016](http://adsabs.harvard.edu/abs/2016MNRAS.456.4425C)).
The particular galaxy sample used to define these voids is the DR7 Luminous Red Galaxy sample of [Kazin et al. (2010)](http://adsabs.harvard.edu/abs/2010ApJ...710.1444K).
If you use this void catalog in a paper, please cite this paper:\
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


</div>