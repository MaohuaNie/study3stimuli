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


- 
### Difference Columns
- **`skewness_diff`**: Difference in skewness between simple options A and B.  
- **`new_skewness_D`**: Difference in skewness between complex equivalents A and B.  
- **`EVD`**: Difference in EV between options A and B (for both simple pairs).
- **`new_EVD`**: Difference in EV between options A and B (for both complex pairs).  
- **`SDD`**: Difference in SD between options A and B (for both simple pairs).
- **`new_SDD`**: Difference in SD between options A and B (for both complex pairs).  

---

## Key Insights

### Using Study 2 Stimuli (`study3_trials_old`)
- The stimuli in this dataframe are based on those used in **Study 2**. I aimed to find **complex equivalents** for the simple options while maintaining similar **expected value (EV)**, **standard deviation (SD)**, and **skewness**. 
- While I successfully generated complex equivalents for most trials that matched EV, SD, and their differences (**EVD** and **SDD**), it was much harder to achieve similar **skewness**.  
  - **Observed skewness issue**:  
    - The absolute skewness of the complex equivalents (**new_skewness_A**, **new_skewness_B**) is almost always lower than the absolute skewness of the simple options (**skewness_a**, **skewness_b**).  
    - This occurs because the constraints of maintaining similar EV and SDD force the complex equivalents to be less skewed.  
  - **Missing rows**:  
    - For two trials, no suitable complex equivalents were found for either option A or B. These rows are missing in the dataframe.  

### Using Newly Generated Stimuli (`study3_trials_new`)
- To address the challenges in matching skewness with Study 2 stimuli, I generated a completely new set of stimuli. These new trials allow for better alignment across **EV**, **SD**, and **skewness**. As previously, the EV and SD were not big problems. 
- **Advantages of the new stimuli**:  
  - The skewness values of the complex equivalents:  
    - **Right-skewed options**: skewness > **1.7**  
    - **Left-skewed options**: skewness < **-1.7**  
    - **Non-skewed options**: skewness between **-0.7 and 0.7**  
  - After applying the **probability weighting function** (Prelec 1 with alpha = .6), the EU changed also in the expected direction for all trials.
      
- **Skewness constraints remain**:  
  - Even with the new stimuli, the absolute skewness values of the complex equivalents are consistently lower than those of the simple options due to the constraints of matching EV and SD.


### My personal preference
- I would prefer using the newly generated stimuli (`study3_trials_new`). While they are not directly derived from Study 2, they align better with the study’s core objectives of maintaining similar EV, SD, and skewness between the simple and complex options.  
---

