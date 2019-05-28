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

#### 3D (ish) model

This example is based on the marmousi model by extending the original 2D model along the 
strike direction. 

The kernel for orthorhombic media is enabled through the runfile as

```
Anisotropy      : ORT
ORT Units       : percent
```

Do not use tilt nor azimuth angles in the current version.

