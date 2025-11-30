
# Health Data Analysis in R: Correlation, Regression, and ANOVA Techniques

This analysis used the **Whitehall FoSSA Study** dataset, a simulated cohort inspired by the original Whitehall Study of Civil Servants. The dataset includes **4,327 participants** followed from 1997 to 2005, with information on cardiovascular risk factors, including BMI, blood pressure, cholesterol, and smoking status.

---

## Steps Taken

1. **Data Preparation and Exploration**
   - Imported and inspected the dataset for structure, variable types, and missing values.  
   - Categorized BMI and other variables to facilitate comparisons across groups.  

2. **Correlation Analysis**
   - Examined the relationship between **BMI and systolic blood pressure (SBP)** using scatterplots and Pearson correlation.  
   - Observed a **very weak positive correlation** (r = 0.085, p < 0.001), indicating BMI explains only a small fraction of SBP variability.  

3. **One-Way ANOVA**
   - Compared SBP across four BMI categories.  
   - Found statistically significant differences between groups (p = 0.0001), confirming SBP varies with BMI.  

4. **Linear Regression Models**
   - **Continuous BMI predictor:** Each one-unit increase in BMI associated with a 0.46 mmHg increase in SBP. Model had very low predictive power (Adj. R² <1%).  
   - **Categorical BMI predictor:** Obese participants had on average 3.7 mmHg higher SBP than normal-weight participants (95% CI: 1.7–5.6, p<0.001).  
   - **Multiple regression adjusting for LDL-C:** Overweight individuals had 1.91 mmHg higher SBP than normal-weight participants after adjustment (95% CI: 0.80–3.02, p=0.001).  
   - **Additional adjustment for smoking status:** Association for obese participants remained significant (3.7 mmHg higher SBP; 95% CI: 1.74–5.63). Smoking status itself was not statistically significant.  

5. **Model Evaluation**
   - Conducted **F-tests** to assess the collective contribution of BMI, LDL-C, and smoking to the model. All variables significantly improved model fit.  
   - Checked assumptions of regression:
     - Normality of residuals (Q–Q plot and histogram)  
     - Influence points/outliers (no significant issues)  
     - Homoscedasticity (residuals vs. fitted plot showed no pattern)  

---

## Key Findings

- BMI is positively associated with SBP, but it explains only a **small fraction of the variability**.  
- SBP increases consistently across BMI categories, with obese individuals showing the highest average SBP.  
- Adjusting for LDL-C and smoking status slightly modifies the associations but does not eliminate them.  
- While statistically significant, the effect sizes suggest that **other factors besides BMI contribute substantially to SBP**.  
- Regression diagnostics indicate the models are appropriate, with no major violations or influential points detected.

---

## Summary

This analysis demonstrates the use of **correlation, ANOVA, and multiple regression techniques** to explore relationships in health data. It highlights the importance of **both statistical significance and practical effect size** when interpreting results in epidemiological studies.

---

## References

Clarke et al. (2007), *Arch Intern Med*, 167(13) — details of the original Whitehall Study that inspired this dataset.
