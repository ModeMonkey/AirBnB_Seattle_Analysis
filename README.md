# AirBnB_Seattle_Analysis

## Libraries used:

 - pandas     - Data manipulation, visualization through grids
 - numpy      - Date manipulation
 - sklearn    - Statistical analysis
 - datetime   - Built-in python library for date manipulation
 - tqdm       - Visualize iteration position
 - ast        - Built-in python library 
 - re         - Regex library
 - matplotlib - Visualize data through graphs
 
Jupyter Notebook and an Anaconda environment were also used during this analysis.

## Motivation:
 
An effort to determine if characteristics of an AirBnB listing can be used with linear regression to predict if a listing will be available on one of the U.S. federal holidays.  While there are other holidays, U.S.federal holidays were picked as they are significant enough in the U.S. to be likely observed in the data of a U.S. city vs. a holiday that is not as observed in the United States. 

## Files:

 - Code.ipynb - A Jupyter Notebook that explains the steps taken in the analysis
 
## Analysis Results:

Results determine that linear regression provides only a nine percent increase in ability to predict a listing's availability (78% accurate) vs. always stating the the listing is available (69% accurate).  A significant number of features don't appear to positively influence the ability to predict a listing's availability on a particular holiday, such as most amenities, neighborhoods, street name, zip code, property type, and various information on the host. 

The analysis also indicated that there is an increase in AirBnB availability on holidays throughtout 2016.  The trend appears to remain when removing listings that were created after the start of 2016.  Furthermore, a majority of listings are available during all U.S. federal holidays, indicating the property may be either always available by the host as a cash-generating property or the host travels during the holidays and makes the property available during those travels. 

## Future Analytical Steps:

Continued analysis on different date ranges and/or regions will provide insight if features of a listing can be used to accurately predict a listing's availability on a federal holiday.

## Process:

The CRoss Industry Standard Process for Data Mining (CRISP-DM) is a process model that serves as the base for a data science process. It has six sequential phases:

### Business understanding – What does the business need?

We need to determine which data is required to determine if a listing's characteristics can be used to predict a holiday's abilability.  This required combinding a listing's characteristics with a listing's availability on a specific day.  As is, those two pieces of data are availabile in two seperate datasets.

### Data understanding – What data do we have / need? Is it clean?

The data we have is:

 - a listing's availability throughout the year
 - a listing's characteristics
 - a listing's reviews

Some of the data needs cleaning - Amentities are in an improper set format saved as a set, dates are strings instead of datetime objects, etc.

Data needed but not available is when a listing was made available/taken off the market.

### Data preparation – How do we organize the data for modeling?

Data from a listing's availability on a particular holiday is mapped into a table of a listing's characteristics.  

### Modeling – What modeling techniques should we apply?

Linear regression

### Evaluation – Which model best meets the business objectives?

Many features do not improve the results generated from linear regression.  These typically include features that are mostly NaN or have too many possible variables per feature.  Using every possible feature, 

A best found model involes the following features per listing:

 ['accommodates',
 'bathrooms',
 'bedrooms',
 'beds',
 'price',
 'weekly_price',
 'monthly_price',
 'security_deposit',
 'cleaning_fee',
 'guests_included',
 'extra_people',
 'minimum_nights',
 'maximum_nights',
 'availability_30',
 'availability_60',
 'availability_90',
 'availability_365',
 'number_of_reviews',
 'review_scores_rating',
 'review_scores_accuracy',
 'review_scores_cleanliness',
 'review_scores_checkin',
 'review_scores_communication',
 'review_scores_location',
 'review_scores_value',
 'host_listings_count',
 'host_total_listings_count',
 'amenity_Wireless Internet',
 'amenity_Smoke Detector',
 'amenity_Heating',
 'amenity_TV',
 'amenity_Washer',
 'amenity_Carbon Monoxide Detector',
 'amenity_Fire Extinguisher',
 'amenity_Shampoo',
 'amenity_Kitchen',
 'amenity_Essentials',
 'amenity_Free Parking on Premises',
 'amenity_Internet',
 'amenity_Dryer',
 'amenity_Family/Kid Friendly',
 'bed_type_Real Bed',
 'host_location_Seattle, Washington, United States',
 'host_acceptance_rate_100%',
 'host_has_profile_pic_t',
 'host_identity_verified_t']


These features indicate that a unit's general availability, the host's profile, general characteristics of the unit, and a select number of amenities are the largest contributors in the ability to predict a unit's availability on a given holiday. 

### Deployment – How do stakeholders access the results?

The results at this stage are too infantile to be of use to stakeholders.  The results are also not significantly better than stating that the property will be available by default - only a nine percent increase. 

### Licensing, Authors, and Acknowledgements

Data Source: AirBnB Seattle data on Kaggle
Source link: [https://www.kaggle.com/datasets/airbnb/seattle](https://www.kaggle.com/datasets/airbnb/seattle)
License: CC0: Public Domain
Achnowledgement: This dataset is part of Airbnb Inside, and the original source can be found here: [http://insideairbnb.com/get-the-data/](http://insideairbnb.com/get-the-data/)
