# WSTDashboard
This repository includes the code used for creating sales tracking datasets that organizes the teams and their target progress.

INTRODUCTION
The objective of this function is to create tabular data used for creating a Weekly Sales Tracker. Note there is a function for quarterly info, and a separate one for annual.

Tableau Server Team/Rep Performance Sales Table is downloaded and fed into this function. It takes in current number of billing days, and today's date. Quarterly also takes in quarter number, and yearly takes in total number of billing days (251 in 2022).

The function knows the finalized targets for each team, and uses this in conjunction with the imported sales data to create a dataframe; it also automatically performs calculations for all columns requested:
   * QTD/YTD Target
   * % to QTD/YTD Target 
   * % Growth PY
   * % to Quarter/Annual Target
    
The function automatically displays the table it has created, as well as download that table as a CSV file to same path as this notebook. 

From there, the Power BI file is refreshed with the new data source.

## Data Acquisition

**Team/Rep Sales Performance**

Explore / Territory Leadership / West Zone Daily Sales (2022) Territory / Team/Rep Performance / 
Download Team_Rep Sales Table_crosstab

Following filters:
* QTD or YTD 
* Financial Sales
* Product Groups: CEMENT, EXTREMITIES, FOOT & ANKLE, HIPS, KNEES, RESTORATIVE THERAPY, SPORTS MEDICINE, TRAUMA
* Team/Rep Name: JOHN KOEHLER, MATT BORROR, RYAN FURNISH, TEAM BLAKE ROBERTS, TEAM DOSSIE LAYTON, TEAM LUNA, TEAM MIDAS, TEAM NEO, TEAM OKC, TEAM RICK ATCHISON, TEAM SEVE SANCHEZ, TEAM SOUTHWEST, TEAM TULSA
* Direct Comparison and 2021 as PY
* Today's date selected

.txt file converted to .csv UTF-8
