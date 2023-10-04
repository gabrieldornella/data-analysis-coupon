Will a Customer Accept the Coupon?

About the Data

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). 

Summary of findings

The dataset has 12684 rows and 26 columns
There are 6 columns with missing data: Car, Bar, CoffeHouse, CarryAway, RestaurantLessThan20, Restaurant20to50
- Percentage of Car rows that are missing data 99.14853358561967%
- Percentage of Bar rows that are missing data 0.8435824660990224%
- Percentage of CoffeeHouse rows that are missing data 1.7108167770419427%
- Percentage of CarryAway rows that are missing data 1.1904761904761905%
- Percentage of RestaurantLessThan20 rows that are missing data 1.0249132765689057%
- Percentage of Restaurant20To50 rows that are missing data 1.490066225165563%
* Considering that more than 99% of the rows have null values in the Car column, this column was removed from the dataset as it will not add much to the analysis.


Acceptance rate
Proportion of the total observations chose to accept the coupon: 56.84%

Relationship between Coupon type and Acceptance Rate
The acceptance rate for coupon types Carry out & Take away and Restaurant(<20) are higher than the overall average (56.84%), both greater than 70%.
The acceptance rate for coupon types Coffee House, Restaurant(20-50) ana Bar are lower than the overall average (56.84%), all lower than 50%.

Temperature
The dataset has only three possible temperatures (80, 55, 30).
80: 51.466414380321666% of total obsevations
55: 30.274361400189214% of total obsevations
30: 18.25922421948912% of total obsevations
Apparently temperature is not an extremely important factor in coupon acceptance. Perhaps because we have few temperature measurements (only three).

Investigating the Bar Coupons
The proportion of bar coupons that were accepted is 41%
Based on these observations, I hypothesize that drivers who accepted the bar coupons are driver who:
- Go to bar more than once and are below 25 years old (Acceptance rate: 69.52%)
- Go to bar more than once and passanger not kid and occupations other than farming, fishing, or forestry. (Acceptance rate: 71.32%)
- Go to bars more than once a month, had passengers that were not a kid and were not widowed (71.79%)
- Go to bars more than once a month and are under the age of 30 (Acceptance rate: 71.79%)

Relationship between Weather and Acceptance Rate
Taking into account the overall acceptance rate of 56.84%, it seems that weather conditions play a role in influencing acceptance rates. Specifically, on sunny days, the acceptance rate sees a slight improvement at 59%, whereas during snowy and rainy weather, the acceptance rates dip to 47% and 46%, respectively.
The observations suggest that weather conditions do indeed influence the acceptance rates of different coupons:**

High Acceptance Rates (Between 60% and 80%):
- "Sunny - Restaurant(<20)" and "Sunny - Carry out & Take away" both exhibit high acceptance rates, with values exceeding 76%.
- "Snowy - Carry out & Take away" also shows a relatively high acceptance rate at approximately 70.68%.
- "Rainy - Carry out & Take away" has a moderate acceptance rate of around 61.13%.

Moderate Acceptance Rates (Between 50% and 60%):
- "Sunny - Coffee House" has an acceptance rate of approximately 50.36%, falling into the moderate range.
- "Sunny - Restaurant(20-50)" and "Sunny - Bar" have acceptance rates around 46.43% and 44.14%, respectively, placing them in this category.

Low Acceptance Rates (Below 50%):
- "Snowy - Restaurant(<20)" has an acceptance rate below 50% at about 48.67%.
- "Snowy - Coffee House," "Rainy - Restaurant(<20)," and "Rainy - Restaurant(20-50)" all have acceptance rates below 45%, indicating lower performance.
- "Rainy - Coffee House," "Rainy - Bar," "Snowy - Bar," and "Snowy - Restaurant(20-50)" have the lowest acceptance rates, with values below 40%.

In summary, Sunny days generally leading to higher acceptance rates, while rainy and snowy conditions tend to result in lower acceptance rates for most coupon types. These insights can be valuable for marketing and promotion strategies based on weather forecasts.

Relationship between Destination and Acceptance Rate
Taking into account the overall acceptance rate of 56.84%, it seems that destination plays a role in influencing acceptance rates. Specifically, people driving to No Urgent Place are more likely to accept the coupon, whereas people driving to Home or Work, the acceptance rates reduce to 50%.
Acceptance rates for different combinations of destinations and coupons shows interesting insights.

High Acceptance Rates:
- "No Urgent Place - Restaurant(<20)" has the highest acceptance rate at approximately 79.25%.
- "Home - Carry out & Take away" also shows a high acceptance rate of nearly 78.87%.
- "No Urgent Place - Carry out & Take away" follows closely with an acceptance rate of about 76.28%.

Moderate Acceptance Rates:
- "Work - Carry out & Take away" has a moderate acceptance rate of around 65.49%.
- "Work - Restaurant(<20)" is another combination with a moderate acceptance rate of about 58.29%.
- "No Urgent Place - Coffee House" and "Home - Restaurant(<20)" also fall into this category with acceptance rates around 58.10% and 55.53%, respectively.

Lower Acceptance Rates:
- "No Urgent Place - Restaurant(20-50)" has a lower acceptance rate of approximately 50.24%.
- "Home - Bar" and "Work - Coffee House" both have acceptance rates below 46%.
- "Home - Restaurant(20-50)" and "No Urgent Place - Bar" have acceptance rates below 44%.
- "Work - Restaurant(20-50)" and "Work - Bar" have the lowest acceptance rates, below 40%.
- "Home - Coffee House" has an acceptance rate of about 36.21%.

This information can be valuable for decision-making related to marketing and promotions as it highlights which combinations of destinations and coupons are performing well in terms of acceptance rates and which ones may need improvement.

Acceptance rate for Restaurant(<20) coupon and Destination is No Urgent Place by occupation

High Acceptance Rates (Above 80%):
Occupations such as "Construction & Extraction," "Production Occupations," "Office & Administrative Support," and "Life Physical Social Science" all have acceptance rates exceeding 80%. "Construction & Extraction" has a perfect acceptance rate of 100%, while others are also quite high.

Moderate to High Acceptance Rates (Between 70% and 80%):
Many occupations fall into this category, including "Sales & Related," "Protective Service," "Architecture & Engineering," "Installation Maintenance & Repair," "Healthcare Support," and "Food Preparation & Serving Related." These occupations have acceptance rates ranging from 70% to just above 80%.

Moderate Acceptance Rates (Between 60% and 70%):
"Community & Social Services," "Computer & Mathematical," "Student," and "Management" have acceptance rates in the range of 69.56% to 81.52%. While some are on the higher side of this range, others are closer to the 70% mark.

Low to Moderate Acceptance Rates (Below 60%):
Occupations like "Transportation & Material Moving," "Business & Financial," "Unemployed," "Education & Training & Library," and "Arts Design Entertainment Sports & Media" fall into this category, with acceptance rates between 50% and 79.51%.

Low Acceptance Rates (Below 50%):
Occupations such as "Healthcare Practitioners & Technical," "Personal Care & Service," "Legal," "Retired," "Farming Fishing & Forestry," and "Building & Grounds Cleaning & Maintenance" have acceptance rates below 70%, with some even below 60% and 50%.

Overall, there is a wide range of acceptance rates across different occupations, with some having very high acceptance rates while others have lower ones. The average acceptance rate across all occupations is stated as 79.25%. Understanding these variations in acceptance rates can be valuable for targeted marketing and outreach strategies tailored to specific occupational groups.