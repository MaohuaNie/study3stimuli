# Study 3 Stimuli

This repository contains the stimuli and dataframes for Study 3, which explores **complex equivalents** for simple options in decision-making tasks. The goal was to create complex lottery pairs based on the simple lottery pairs we used in Study 2, matching them as closely as possible in terms of **expected value (EV)**, **standard deviation (SD)**, and **skewness**.

---

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
- **`EVD`**: Difference in EV between options A and B (for simple pairs).  
- **`new_EVD`**: Difference in EV between options A and B (for complex pairs).  
- **`SDD`**: Difference in SD between options A and B (for simple pairs).  
- **`new_SDD`**: Difference in SD between options A and B (for complex pairs).  

---

## Key Insights

### Using Study 2 Stimuli (`study3_trials_old`)
- The stimuli in this dataframe are based on those used in **Study 2**. I aimed to find **complex equivalents** for the simple options while maintaining similar **expected value (EV)**, **standard deviation (SD)**, and **skewness**.
- **Challenges faced**:  
  - The absolute skewness of the complex equivalents (**new_skewness_A**, **new_skewness_B**) is almost always lower than the absolute skewness of the simple options (**skewness_a**, **skewness_b**). This is due to constraints of maintaining similar EV and SDD.
  - Two trials are missing because no suitable complex equivalents could be found for either option A or B.  

### Using Newly Generated Stimuli (`study3_trials_new`)
- To address the challenges in matching skewness with Study 2 stimuli, I generated a completely new set of stimuli. These new trials allow for better alignment across **EV**, **SD**, and **skewness**.
- **Advantages of the new stimuli**:  
  - Skewness values for complex equivalents:  
    - **Right-skewed options**: skewness > **1.7**  
    - **Left-skewed options**: skewness < **-1.7**  
    - **Non-skewed options**: skewness between **-0.7 and 0.7**  
  - After applying the **probability weighting function** (Prelec 1 with alpha = 0.6), the expected utility differences between simple and complex options also align with theoretical predictions.
- **Remaining challenges**:  
  - As before, the absolute skewness values of complex equivalents are consistently lower than those of simple options due to the constraints of matching EV and SD.

---

### My Personal Preference
- I recommend using the newly generated stimuli (`study3_trials_new`). While these are not directly derived from Study 2, they align better with the study’s core objectives of maintaining similar EV, SD, and skewness between simple and complex options.

---

### Code
- The code used to generate and analyze the stimuli is included in **`stimuli_study3.ipynb`**, but it is computationally intensive.
