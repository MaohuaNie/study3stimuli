# Study 3 Stimuli

This repository contains the stimuli and dataframes for Study 3, which explores complex equivalents for simple options in decision-making tasks. The goal is to create stimuli pairs with similar **expected value (EV)**, **standard deviation (SD)**, and **skewness**, while comparing the original stimuli from Study 2 to newly generated stimuli.

## Files and Description

### Stimuli Files
- **`study3_trials_old_short.csv`**  
  A concise version of the dataframe using stimuli from Study 2 to generate complex equivalents.
  
- **`study3_trials_old.csv`**  
  A detailed version of the dataframe with all trials using Study 2 stimuli.

- **`study3_trials_new_short.csv`**  
  A concise version of the dataframe with newly generated stimuli to ensure better matches in EV, SD, and skewness.

- **`study3_trials_new.csv`**  
  A detailed version of the dataframe with all trials using newly generated stimuli.

### Key Columns
- **Simple Options**:  
  - **`EVA`, `EVB`**: Expected values of simple options A and B.  
  - **`skewness_a`, `skewness_b`**: Skewness of simple options A and B.

- **Complex Equivalents**:  
  - **`new_EVA`, `new_EVB`**: Expected values of complex equivalents for A and B.  
  - **`new_skewness_A`, `new_skewness_B`**: Skewness of complex equivalents for A and B.

- **Difference Columns**:  
  - **`skewness_diff`**: Difference in skewness between simple options A and B.  
  - **`new_skewness_D`**: Difference in skewness between complex equivalents A and B.

## Key Insights
- Complex equivalents often have **lower absolute skewness** than their simple counterparts due to constraints in matching EV and SD.
- **`study3_trials_old`**: Uses Study 2 stimuli, but finding good matches for skewness was challenging. Some rows are missing suitable complex equivalents.
- **`study3_trials_new`**: Newly generated stimuli that better match EV, SD, and skewness.  
  - Right-skewed options: **skewness > 1.7**  
  - Left-skewed options: **skewness < -1.7**  
  - Non-skewed options: **skewness between -0.7 and 0.7**

## Repository Structure
```plaintext
├── study3_trials_old_short.csv
├── study3_trials_old.csv
├── study3_trials_new_short.csv
├── study3_trials_new.csv
└── README.md
