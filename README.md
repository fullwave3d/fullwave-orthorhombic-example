### Example for using the implementation in fullwave for orthorhombic media

Current implementation supports both 2D (effectivey transverse isotropy) and 3D geometry.
Both modelling and inversion can be carried out. When carrying out inversion update for 
velocity only. Jointly updating parameters may yield undesirable results.

#### Get version 700.orth and run

1. Get fullwave cloned into your system

2. Get branch 700.orth (implementation for orthorhombic)

```
git fetch
git checkout 700.orth
```

#### Input files for model parameters

It takes the usual file for Vp with 5 additional files for the parameters of anisotropy

```
Epsilon 1 in -TrueEpsilon.vtr or -TrueEpsilon1.vtr
Epsilon 2 in -TrueEpsilon2.vtr
Delta 1 in -TrueDelta.vtr or -TrueDelta1.vtr
Delta 2 in -TrueDelta2.vtr
Delta 3 in -TrueDelta3.vtr
```


#### 3D (ish) model

This example is based on the marmousi model by extending the original 2D model along the 
strike direction. 

The kernel for orthorhombic media is enabled through the runfile as

```
Anisotropy      : ORT
ORT Units       : percent
```

Do not use tilt nor azimuth angles in the current version.



