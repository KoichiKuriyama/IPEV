# IPEV Model

The integer programing extreme value (IPEV) model  accounts the integer property of trip data. The IPEV model is consistent with utility theory and provides a single structural framework for simultaneously modeling the choice of alternatives and quantity decisions with the constraint of the integer value of consumption. This model has a closed-form probability expression. This sample files include the estimation code using closed-form or simulation, the demand prediction, the welfare analysis, and the sample dataset.

## Requirement
- GAUSS platform [Aptech](https://www.aptech.com)
- maxlik or maxlikmt [Aptech](https://www.aptech.com)

## Usage
**Estimation:**
- Set the parameters in  **IPEV.gss**
  - **U_FUNCTION**: the utility function
  - For the estimation with closed-form, set the **SIMULATE = 0**
  - For the estimation with simulation, set the **SIMULATE = 1**
- Run the estimation code in the GAUSS 
```
>> run IPEV.gss
```
**Prediction:**
- Set the parameters in  **DEMAND.gss**
  - **U_FUNCTION**: the utility function
  - **B**: vector of estimated parameters
  - **VCOV**: variance-covariance matrix
  - Set secnarios
- Run the prediction code in the GAUSS 
```
>> run DEMAND.gss
```
