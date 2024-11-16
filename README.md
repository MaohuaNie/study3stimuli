I’ve done my best to find the complex equivalents for the stimuli we used in Study 2, aiming to match them closely in terms of expected value (EV), standard deviation (SD), and skewness.

Here are some tips for reading the dataframes:
	•	EVA or original EVA columns represent the simple options.
	•	new_ columns indicate the complex equivalents. For example, EVA is the EV of simple option A, while new_EVA is the EV of its complex equivalent.

If you have time, you can review the attached files:
	•	study3_trials_old_short (or for more detail: study3_trials_old) – Here, I used the stimuli from Study 2 to generate the complex equivalents.

For most trials, I managed to find complex equivalents with similar EV, SD, EVD, and SDD. However, achieving similar skewness proved challenging:
	•	The skewness differences between the simple options (columns skewness_a and skewness_b) and their complex equivalents (new_skewness_A and new_skewness_B) are noticeable.
	•	The absolute skewness values of the complex equivalents are almost always lower than those of the simple options. I believe this is due to the constraints imposed by matching EV and SDD.
	•	Additionally, I couldn’t find suitable complex equivalents for two rows, meaning options A or B are missing in those cases.

To address these issues, I generated new stimuli (study3_trials_new_short, or for more detail: study3_trials_new). These trials better balance EV, SD, and skewness. While the skewness of the complex equivalents remains consistently less extreme than their simple counterparts, the following ranges are met:
	•	Right-skewed options: skewness > 1.7
	•	Left-skewed options: skewness < -1.7
	•	Non-skewed options: skewness between -0.7 and 0.7

Additionally, after applying the probability weighting function, the differences between the simple and complex options align with expectations.

I’m unsure which trial set we should use. Personally, I prefer the new stimuli for the following reasons:
	1.	We’ve already used different stimuli in the first two studies, so introducing new ones here isn’t an issue.
	2.	It’s nearly impossible to find complex equivalents for the simple stimuli from Study 2 that preserve EV, SD, and skewness simultaneously. Using new stimuli ensures we maintain these core characteristics.

Please share any feedback or comments. The dataframes are also available on GitHub for your review.

Looking forward to hearing your thoughts!
