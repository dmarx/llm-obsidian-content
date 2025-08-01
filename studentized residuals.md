---
date: 1713907828.295046
tags:
- autogenerated
- source__oai
- conversation_id__9f8c6c88-3adc-4b4b-af9c-e569eada9468
- msg_aaa2cc34-bffe-4f3d-b333-63293596dbd2
- msg_652d5f1c-e47f-4392-888b-1e43f8fe984b
- colorclass/energy-dissipation
title: studentized residuals
---

**USER**

studentized residuals


**ASSISTANT**

Studentized residuals are a key diagnostic tool in regression analysis, used to assess the fit of data points within a regression model and identify outliers. They are a type of standardized residual that provide a more robust basis for comparison across data points by accounting for differences in variance, which regular residuals do not.

### Definition of Studentized Residuals

There are two types of studentized residuals: internally and externally studentized residuals. Both types aim to scale the raw residuals by an estimate of their standard deviation, but they differ in how this standard deviation is calculated.

1. **Internally Studentized Residuals**:
   Internally studentized residuals are calculated by dividing each raw residual by an estimate of its standard error, where the standard error is estimated from the same model that produced the residual. The formula for the \(i\)-th internally studentized residual \(r_i\) is:

   $$
   r_i = \frac{e_i}{s \sqrt{1-h_{ii}}}
   $$

   Here, \(e_i\) is the raw residual for the \(i\)-th observation, \(s\) is the estimated standard deviation of the residuals (usually the square root of the [[mean squared error]] of the regression), and \(h_{ii}\) is the leverage of the \(i\)-th observation from the [[hat matrix]].

2. **Externally Studentized Residuals**:
   Externally studentized residuals (or deleted residuals) are similar to internally studentized residuals but with a crucial difference: each residual is standardized using an estimate of its standard deviation computed from a model that has the \(i\)-th observation deleted. This approach helps in assessing the influence of each observation on the model. The formula for the \(i\)-th externally studentized residual is:

   $$
   t_i = \frac{e_i}{s_{(i)} \sqrt{1-h_{ii}}}
   $$

   where \(s_{(i)}\) is the standard deviation of the residuals from the regression model fitted without the \(i\)-th observation.

### Uses and Importance

- **Detection of Outliers**: Studentized residuals are used to identify outliers in data. Observations whose studentized residuals are greater than about 2 or 3 in absolute value are typically considered potential outliers, as these values would be expected to occur infrequently under a normal distribution (less than about 5% of the time if the cutoff is 2, and less than 1% if the cutoff is 3).
  
- **Assessment of Model Fit**: Large studentized residuals can indicate areas where the model does not fit the data well. This might suggest the need for model modifications, such as including additional explanatory variables, considering interaction effects, or using non-linear models.

- **Influence of Observations**: Externally studentized residuals are particularly useful for evaluating the influence of each observation on the fitted model, as they show how much each residual would change if the observation were omitted.

### Visualization

Studentized residuals are often plotted against fitted values or other variables to check for patterns that indicate problems with the model, such as non-constant variance (heteroscedasticity), non-linearity, or the influence of outliers.

### Conclusion

Studentized residuals provide a more standardized and rigorous method for assessing the quality of fit and the influence of observations in regression analysis compared to raw residuals. They are an essential part of the diagnostic toolkit for statisticians and analysts, helping to ensure that regression models are robust, reliable, and well-suited to the data.


---

preceding: [[cook's distance]]  


following: [[leverage from the [[hat matrix]].]]