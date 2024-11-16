# Study 3 Stimuli

This repository contains the stimuli and dataframes for Study 3, which explores **complex equivalents** for simple options in decision-making tasks. The goal was to create complex lottery pairs based on the simple lottery pairs we used in Study 2, matching them as closely as possible in terms of **expected value (EV)**, **standard deviation (SD)**, and **skewness**.

---

## Files and Description

### Stimuli Files
- [**`study3_trials_old_short.csv`**](study3_trials_old_short.csv)  
  A concise version of the dataframe using stimuli from Study 2 to generate complex equivalents, focusing on key trials.

- [**`study3_trials_old.csv`**](study3_trials_old.csv)  
  A detailed version of the dataframe with all trials using Study 2 stimuli. This file contains the same trials as the short version but includes additional details for each trial.

---

## Key Columns in Dataframes

### Simple Options
- **`EVA`, `EVB`**: Expected values of simple options A and B.  
- **`SDA`, `SDB`**: Standard deviations of simple options A and B.  
- **`simple_skewness_a`, `simple_skewness_b`**: Skewness of simple options A and B.  

### Complex Equivalents
- **`complex_EVA`, `complex_EVB`**: Expected values of complex equivalents for A and B.  
- **`complex_SDA`, `complex_SDB`**: Standard deviations of complex equivalents for A and B.  
- **`complex_skewness_A`, `complex_skewness_B`**: Skewness of complex equivalents for A and B.

### Difference Columns
- **`simple_skewness_D`**: Difference in skewness between simple options A and B.  
- **`complex_skewness_D`**: Difference in skewness between complex equivalents A and B.  
- **`EVD`**: Difference in EV between options A and B (for simple pairs).  
- **`complex_EVD`**: Difference in EV between options A and B (for complex pairs).  
- **`SDD`**: Difference in SD between options A and B (for simple pairs).  
- **`complex_SDD`**: Difference in SD between options A and B (for complex pairs).  

---

## Key Insights

### Using Study 2 Stimuli ([`study3_trials_old`](study3_trials_old_short.csv))
- The stimuli in this dataframe are based on those used in **Study 2**. I found the  **complex equivalents** for the simple options while maintaining similar **expected value (EV)**, **standard deviation (SD)**.

- **Challenges faced**:  
  - The absolute skewness of the complex equivalents (**complex_skewness_A**, **complex_skewness_B**) is almost always lower than the absolute skewness of the simple options (**skewness_a**, **skewness_b**). This is due to constraints of maintaining similar EV and SDD. 
  - However, the absolute skewness of the complex equivalents of right skewed option are always above 0.7 and the left skewed option are always below -0.7, and the non skewed options are almost all in range -0.7 to 0.7.
  
  
the EU after applying the probability weighting function with alpha = 0.6 are also not very bad (in ns trials are not so good, but in rl and lr almost perfect.).

---

### My idea
- I think we can use the trials are good to use in study 3 even the skewness of new generated complex options are not perfect and also the EU in ns trials.

---

### Code
- The code used to generate and analyze the stimuli is included in [**`stimuli_study3.ipynb`**](stimuli_study3.ipynb), but it is computationally intensive.
