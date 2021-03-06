# School District Analysis

## Overview

### Purpose

Maria has been tasked with analyzing information about standardized test data to help facilitate informed discussions surrounding standardized testing in schools and school funding.  During this process the school board has determined there is evidence of academic dishonesty, and Maria has asked us to help remove the compromised data and rework the analysis.

### Resources

- Python, pandas, numpy
- schools_complete.csv
- students_complete.csv

## Results

### How is the district summary affected?

Old district summary:
![old_district_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_district_summary.JPG)

New district summary:
![district_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/district_summary.JPG)

As seen above, there is a slight difference between the old and new district summaries.  The average math scores, passing math percentages, passing reading percentages, and overall passing percentages had small decreases.

### How is the school summary affected?

Old school summary (before ninth-grade scores are removed):
![THS_school_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/THS_school_summary.JPG)

New school summary (after ninth-grade scores are removed):
![THS_school_summary_no_ninth_graders.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/THS_school_summary_no_ninth_graders.JPG)

Prior to the removal of ninth-grade scores, the percentage of passing math, passing reading, and overall percentages were all much lower in value (67%, 70%, and 65% respectively).  Once the ninth-grade scores were removed, all of these percentage values went up (93%, 97%, and 91% respectively).

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Old top and bottom 5 schools:
![old_high_low_performing_schools.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_high_low_performing_schools.JPG)

New top and bottom 5 schools:
![high_low_performing_schools.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/high_low_performing_schools.JPG)

While the average math and reading scores and the percentage of passing math and reading scores for Thomas High School decreased, the decrease was tiny and did not affect the overall ranking of Thomas High School in comparison to the other schools.

### How does replacing the ninth-grade scores affect the following:
 
#### Math and reading scores by grade

Old math scores by grade:                
![old_avg_math_scores.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_avg_math_scores.JPG)

New math scores by grade:                
![avg_math_scores.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/avg_math_scores.JPG)

Old reading scores by grade:                 
![old_avg_reading_scores.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_avg_reading_scores.JPG)

New reading scores by grade:                 
![avg_reading_scores.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/avg_reading_scores.JPG)

Replacing the ninth-grade scores did not affect the math and reading scores of the other grades at Thomas High School.  It also did not impact the other schools.  The tables above show that only the ninth-grade scores of Thomas High School students were impacted.

#### Scores by school spending

Old scores by school spending:
![old_spending_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_spending_summary.JPG)

New scores by school spending:
![spending_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/spending_summary.JPG)

As can be seen above, removing ninth-grade scores had no impact on school spending.

#### Scores by school size

Old scores by school size:                
![old_size_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_size_summary.JPG)

New scores by school size:
![size_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/size_summary.JPG)

As can be seen above, removing ninth-grade scores had no impact on overall scores by school size.

#### Scores by school type

Old scores by school type:                 
![old_type_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/old_type_summary.JPG)

New scores by school type:
![type_summary.JPG](https://github.com/mathur-nikita/School_District_Analysis/blob/main/screenshots/type_summary.JPG)

As can be seen above, removing ninth-grade scores had no impact on overall scores by type of school.

## Summary

1) Once all ninth-grade scores were replaced with NaNs ("Not a Number" values), the total percentage of students who passed dropped dramatically.  This is because the number of ninth-graders is still included in all calculations.  In order to have clean data for correct calculations it's not enough to just remove their grades, the students themselves should not be considered.  All calculations for Thomas High School should take place with tenth, eleventh, and twelfth grade students only.

2) Once ninth-grade students are completely removed from the dataset, it can be seen that the overall district summary was not greatly impacted - the difference in values is tiny.

3) The ranking of Thomas High School was also not impacted - it is still ranked second compared to all other schools within the same district, even though it can be seen that the average scores and passing percentages changed slightly.

4) Removal of ninth-grade scores did not impact the following metrics:
- scores by school spending
- scores by school size
- scores by school type

This is possibly the result because the difference in values of the scores before and after removal is so small.
