# DS4002_Project2
Gerrymandering Image Analysis

## Contents
1. SRC
2. Data
3. Figures
4. References

## SRC
### Installing Code
We used Python version 3.8.8. The packages used were numpy version 1.20.1, pandas version 1.2.4 , Pillow version 8.2.0, and
scipy version 1.6.2.
### Usage
We first started by loading in the images of the states. We found the pixel count for blue, red, and purple for each state with current district boundaries. Next we found counts of pixels for each shade of blue, red, and purple for each state with hypothetical non-gerrymandered district boundaries. We then performed a chi-squared test using these counts for each state to determine if there is a significant difference in counts for current vs. non-gerrymandered districts. To verify our model, we loaded in and cleaned the data from Dave's Redistricting congressional votes for each state's districts. We then calculated the declination angle which verifys whether or not gerrymandering has occurred. We then compared our results with the declination angle results to test the accuracy of our results. 

## Data
FiveThirtyEight Data
|Variable              |Descritpion                                        |
| -------------------- | ------------------------------------------------- |
| usually_democratic   | Percent chance of being reresented by a Democrat  |
| usually_republican   | Percent chance of being reresented by a Republic  |
| highly_competitive   | Percent chance of being reresented by a Rep or Dem|

Congressional Data
|Variable              |Descritpion                                        |
| -------------------- | ------------------------------------------------- |
| ID                   | identification of the district within the state   |
| Total pop            | total population within the district              |
| Dem                  | percentage of Democratic lean within the district |
| Rep                  | percentage of Republican lean within the district |

To acquire state data, we are using FiveThirtyEight's “The Gerrymandering Project.” The project also provides district boundaries of the states that match the partisan breakdown of seats to the electorate to compare with the actual boundaries. To validate our model we used  the 2022 congressional map of the states from Dave's Redistricting 2020 website.

The images we used can be found at this link: https://drive.google.com/drive/folders/1FocnYOfHYInz-Hoalg1t-OfzWHOFYZAX?usp=sharing
## Figures
### Figures Table
|State        | P-Value     | Interpretation            | Declination Angle   |
|-------------|-------------|---------------------------|---------------------|
|Virginia     |   0.0       |There is gerrymandering    | 0.37^*              |
|New Mexico   |    1        |There is no gerrymandering | -0.17               |
|Massachusetts|   0.0       |There is gerrymandering    |                     |
|Alabmama     |   0.0       |There is gerrymandering    |0.55^*               |
|Nevada       |    1        |There is no gerrymandering |-0.35                |


## References
Hendricks, T. (2021, December 10). Detecting and measuring gerrymandering with python. Medium. https://towardsdatascience.com/detecting-and-measuring- gerrymandering -with-python-f85a1315acd4 

Bycoffe, A., Koeze, E., Wasserman, D., & Wolfe, J. (2018, January 25). The Atlas Of Redistricting. FiveThirtyEight. https://projects.fivethirtyeight.com/ redistricting- maps/virginia/
