# IEC 61499 Delta Modeling Case Studies Repository

This repository contains the accompanying material to the paper __Delta Modeling in IEC 61499: Expressing Control Software Variability of Cyber-Physical Product Systems__.

IEC~61499 is a standard for developing industrial distributed control software. It supports the configurability of the control software as the application model is platform-independent and separated from the hardware configuration specification. It is thus a good basis to develop control software for highly configurable Cyber-Physical Production Systems (CPPSs). Systematically managing the control software variability in CPPSs would help to increase reuse and reduce the cost of developing and/or maintaining CPPSs.

In this paper, we propose an approach to systematically manage IEC~61499-based control software using a (textual) delta modeling approach.
The delta modeling approach is a prominent concept in the Software Product Line (SPL) domain for expressing and maintaining software variability.
We show how our delta modeling approach can express control software variability and provide a semi-automatic control software generator. The results confirm that our delta modeling approach can be helpful for implementing and maintaining IEC~61499-based control software variability.

## Organization of the repository

The repository contains five use cases:

- [Capping Station](cappingstation) by courtesy of Alois Zoitl in [his publication](https://ieeexplore.ieee.org/document/6622910)
- [Truck](TruckProdStruct) by courtesy of [Tu Prague](https://testbed-test.ciirc.cvut.cz)
- [Shift fork](ShiftForkPL) by courtesy of our industry partner
- [Rocker switch](RockerswitchPL) by courtesy of our industry partner
- [Waterfilter](WaterfilterPL) by courtesy of [Askwar Hilonga](https://gongali.wordpress.com/the-water-nanofilter/)

Each use case follows the following structures:

- `core`: This folder contains a 4diac project representing a base implementation for a production system in each case study.
- `delta`: This folder contains one or more Delta Model to adjust the base implementation into a specific production system variant. This folder also contains a `DeltaConfiguration` file which define a mapping between one or more delta models into a feature inside a [FeatureIDE](https://featureide.github.io/) feature model.
- `SPLConfig`: This folder contains multiple configuration setup for the [Variability for 4diac (V4rdiac) tool](https://dl.acm.org/doi/abs/10.1145/3503229.3547028).
- `variabilityModels`: This folder contains one or more feature models describing the variability of a production system for each case study.
