# Texas-TriValve-1.1
The Texas TriValve 1.1 is a second patient-specific, high fidelity finite element model of the human tricuspid valve. We follow the same approach as described in Mathur et. al. 2022 to build this second unique model, with several important changes from the Texas TriValve 1.0 noted below.

## Model Updates
* Updated the element formulation to linear quadrilateral reduced-integration shell elements (Abaqus S4R).
* The finite element mesh represents the valve's midsurface.
* The friction coefficient has been changed to 0.01.
* A linear pressure-overclosure relationship is used for the contact formulation.
* The linear bulk viscosity coefficient has been changed to 5.0.

## Code Description
We provide Abaqus input files used to run simulations of the healthy and diseased tricuspid valve. For additional details on simulation settings and element choices please refer to the main text. We also include ParaView visualization toolkit files of the valve simulation. This repository includes the following folders: 

* Healthy_QuasiStatic
  * Healthy tricuspid valve modeled from end-diastole to end-systole.
* Diseased_QuasiStatic
  * Regurgitant tricuspid valve model loaded to pathological pressures at end-systole.

Additionally, we provide a user defined material model (Leaflet_Material.f) that must be used to successfully run the input files listed above. We recommend all models be run in double precision.

## References
If you find this repository useful for your research, please cite the following work:
```
@article{Mathur2022_TTV,
author = {Mathur, Mrudang and Meador, William D. and Malinowski, Marcin and Jazwiec, Tomasz and Timek, Tomasz A. and Rausch, Manuel K.},
doi = {10.1007/s00366-022-01659-w},
isbn = {0123456789},
issn = {0177-0667},
journal = {Engineering with Computers},
keywords = {Annuloplasty,Precision medicine,Predictive simulation,Repair,Transcatheter},
month = {may},
publisher = {Springer London},
title = {{Texas TriValve 1.0 : a reverse-engineered, open model of the human tricuspid valve}},
url = {https://link.springer.com/10.1007/s00366-022-01659-w},
year = {2022}
}


```

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
