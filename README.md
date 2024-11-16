# Study 3 Stimuli

This repository contains the stimuli and dataframes for Study 3, which explores **complex equivalents** for simple options in decision-making tasks. The goal was to create complex lottery pairs based on the simple lottery pairs we used in study 2 with same **expected value (EV)**, **standard deviation (SD)**, and **skewness**,

## Files and Description

### Stimuli Files
- **`study3_trials_old_short.csv`**  
  A concise version of the dataframe using stimuli from Study 2 to generate complex equivalents, focusing on key trials.

- **`study3_trials_old.csv`**  
  A detailed version of the dataframe with all trials using Study 2 stimuli. This file contains the same trials as the short version but includes additional details for each trial.



- **`study3_trials_new_short.csv`**  
  A concise version of the dataframe with newly generated stimuli that ensure better alignment with EV, SD, and skewness criteria.

- **`study3_trials_new.csv`**  
  A detailed version of the dataframe with all trials using the newly generated stimuli. This file includes the same trials as the short version but with more detailed trial-level data.

---

## Key Columns in Dataframes

### Simple Options
- **`EVA`, `EVB`**: Expected values of simple options A and B.  
- **`SDA`, `SDB`**: Standard deviations of simple options A and B.  
- **`skewness_a`, `skewness_b`**: Skewness of simple options A and B.  

### Complex Equivalents
- **`new_EVA`, `new_EVB`**: Expected values of complex equivalents for A and B.  
- **`new_SDA`, `new_SDB`**: Standard deviations of complex equivalents for A and B.  
- **`new_skewness_A`, `new_skewness_B`**: Skewness of complex equivalents for A and B.  

### Difference Columns
- **`skewness_diff`**: Difference in skewness between simple options A and B.  
- **`new_skewness_D`**: Difference in skewness between complex equivalents A and B.  
- **`EVD`**, **`new_EVD`**: Difference in EV between options A and B (for both simple and complex pairs).  
- **`SDD`**, **`new_SDD`**: Difference in SD between options A and B (for both simple and complex pairs).  

---

## Key Insights

1. **Using Study 2 Stimuli (`study3_trials_old`)**:  
   - Matching EV, SD, and skewness was challenging.  
   - In many cases, the complex equivalents have **lower absolute skewness** than their simple counterparts due to constraints in matching EV and SDD.  
   - Some trials are incomplete, as no suitable complex equivalents could be generated for either option A or B.

2. **Using Newly Generated Stimuli (`study3_trials_new`)**:  
   - Newly generated stimuli allow for better alignment across EV, SD, and skewness.  
   - Absolute skewness values for complex equivalents are generally lower than those of simple options. However:  
     - Right-skewed options: skewness > **1.7**  
     - Left-skewed options: skewness < **-1.7**  
     - Non-skewed options: skewness between **-0.7 and 0.7**  
   - After applying the probability weighting function, differences between simple and complex options align with expectations.

3. **General Observation**:  
   - Complex equivalents tend to exhibit less extreme skewness compared to simple options due to the balancing act between EV, SD, and skewness.  

---

