# AirBnB_Seattle_Analysis

Libraries used:

 - pandas     - Data manipulation, visualization through grids
 - numpy      - Date manipulation
 - sklearn    - Statistical analysis
 - datetime   - Built-in python library for date manipulation
 - tqdm       - Visualize iteration position
 - ast        - Built-in python library 
 - re         - Regex library
 - matplotlib - Visualize data through graphs
 
Jupyter Notebook and an Anaconda environment were also used during this analysis.

Motivation:
 
An effort to determine if characteristics of an AirBnB listing can be used with linear regression to predict if a listing will be available on one of the U.S. federal holidays.  While there are other holidays, U.S.federal holidays were picked as they are significant enough in the U.S. to be likely observed in the data of a U.S. city vs. a holiday that is not as observed in the United States. 

Files:

 - Code.ipynb - A Jupyter Notebook that explains the steps taken in the analysis
 
Analysis Results:

Results determine that linear regression provides only a nine percent increase in ability to predict a listing's availability (78% accurate) vs. always stating the the listing is available (69% accurate).  A significant number of features don't appear to positively influence the ability to predict a listing's availability on a particular holiday, such as most amenities, neightbourhoods, street name, zip code, property type, and various information on the host. 

The analysis also indicated that there is an increase in AirBnB availability on holidays throughtout 2016.  The trend appears to remain when removing listings that were created after the start of 2016.  Furthermore, a majority of listings are available during all U.S. federal holidays, indicating the property may be either always available by the host as a cash-generating property or the host travels during the holidays and makes the property available during those travels. 

Future Analytical Steps:

Continued analysis on different date ranges and/or regions will provide insight if features of a listing can be used to accurately predict a listing's availability on a federal holiday.
