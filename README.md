# IPEV Model

The integer programing extreme value (IPEV) model  accounts the integer property of trip data. The IPEV model is consistent with utility theory and provides a single structural framework for simultaneously modeling the choice of alternatives and quantity decisions with the constraint of the integer value of consumption. This model has a closed-form probability expression. This sample files include the estimation code using closed-form or simulation, the demand prediction, the welfare analysis, and the sample dataset.

![Figure1](https://github.com/KoichiKuriyama/IPEV/blob/ea21771ee08a32b8e972ec9692fe57e7b850361b/figure/fig1.png)
Figure 1. Continuous and integer demand models.

## Requirement
- GAUSS platform [Aptech](https://www.aptech.com)
- maxlik or maxlikmt [Aptech](https://www.aptech.com)

## Usage
**Estimation:**
- Set the parameters in  **[IPEV.gss](https://github.com/KoichiKuriyama/IPEV/blob/350163d7f20746fc02f169a37a2c77b7c9745bfd/IPEV.gss)** (required maxlik) or **[IPEVmt.gss](https://github.com/KoichiKuriyama/IPEV/blob/350163d7f20746fc02f169a37a2c77b7c9745bfd/IPEVmt.gss)** (required maxlikmt)
  - **U_FUNCTION**: the utility function
  - For the estimation with closed-form, set **SIMULATE = 0**
  - For the estimation with simulation, set **SIMULATE = 1**
- Run the estimation code in the GAUSS: 
```
>> run IPEV.gss
```
**Prediction:**
- Set the parameters in  **[DEMAND.gss](https://github.com/KoichiKuriyama/IPEV/blob/350163d7f20746fc02f169a37a2c77b7c9745bfd/DEMAND.gss)**
  - **U_FUNCTION**: the utility function
  - **B**: vector of estimated parameters
  - **VCOV**: variance-covariance matrix
  - Set secnarios
- Run the prediction code in the GAUSS: 
```
>> run DEMAND.gss
```
## Manual
For the detail, see **[manual.pdf](https://github.com/KoichiKuriyama/IPEV/blob/350163d7f20746fc02f169a37a2c77b7c9745bfd/manual.pdf)**.

## License
MIT License

## Reference
[Kuriyama, K., Y. Shoji, and T. Tsuge. (2023) The integer programing extreme value (IPEV) model: An application for estimation of the leisure trip demand. NRE Discussion Papers No. 2023-01, Natural Resource Economics, Division of Natural Resource Economics, Graduate School of Agriculture, Kyoto University.](https://repository.kulib.kyoto-u.ac.jp/dspace/bitstream/2433/281531/1/NREDP2023_01.pdf)

## Acknowledgments
- [MDCEV by Chandra R. Bhat](https://www.caee.utexas.edu/prof/bhat/FULL_CODES.htm)
- [rmdcev by Patrick Lloyd-Smith](https://github.com/plloydsmith/rmdcev)
