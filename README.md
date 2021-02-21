# Tanzania Water Points Project

**Working for the Tanzanian Ministry of Water to predict the operating condition of a waterfront.**

# Data
Data was obtain from two data sets: 
* 'train_set_labels.csv'
* 'train_set_values.csv' 

Both from Kaggle. It contained over <b>59k data points and about 40 columns</b>. They are described below.

* amount_tsh - Total static head (amount water available to waterpoint)
* date_recorded - The date the row was entered
* funder - Who funded the well
* gps_height - Altitude of the well
* installer - Organization that installed the well
* longitude - GPS coordinate
* latitude - GPS coordinate
* wpt_name - Name of the waterpoint if there is one
* num_private -
* basin - Geographic water basin
* subvillage - Geographic location
* region - Geographic location
* region_code - Geographic location (coded)
* district_code - Geographic location (coded)
* lga - Geographic location
* ward - Geographic location
* population - Population around the well
* public_meeting - True/False
* recorded_by - Group entering this row of data
* scheme_management - Who operates the waterpoint
* scheme_name - Who operates the waterpoint
* permit - If the waterpoint is permitted
* construction_year - Year the waterpoint was constructed
* extraction_type - The kind of extraction the waterpoint uses
* extraction_type_group - The kind of extraction the waterpoint uses
* extraction_type_class - The kind of extraction the waterpoint uses
* management - How the waterpoint is managed
* management_group - How the waterpoint is managed
* payment - What the water costs
* payment_type - What the water costs
* water_quality - The quality of the water
* quality_group - The quality of the water
* quantity - The quantity of water
* quantity_group - The quantity of water
* source - The source of the water
* source_type - The source of the water
* source_class - The source of the water
* waterpoint_type - The kind of waterpoint
* waterpoint_type_group - The kind of waterpoint

# Observations

## Which structure has the most water points?

![gravity_status](images/one.png)

I wanted to see which type of structure is more popular and most reliable. Looking at the graph:
* Gravity well are the most popular.
* motor pump water points is the only structure that has more non functional water points then functional.
* Gravity pumps are the way to go, seeing that only about 13% are non functional and 5% needs repair.

## Does the quantity affect the status?
![quantity_status](images/two.png)

* We see that enough water is a great predictor for functional wells. 
* Makes sense that dry well have more non functional wells because of the lack of water. 
* Insufficient has an almost balance between functional and non functional. It might suggest that the wells with a little bit left are still functional whereas the ones that doesn't have any aren't functional anymore.

* So our best bet to finding functional wells would be quantity enough and dry for finding non functional wells.

## Does location play a role?

I wanted to see if different areas affected the status of wells.
![loc_image](images/three.png)

![loc_image](images/zones.webp)

![zone_image](images/four.png)

So majority of the wells are located in Lake and South highland zones. These zones can possibly be located near bodies of water such as lakes, which can provide a good source of water. Zones like central are a little ways away from large water sources, therefore not many wells are installed there. However it's hard to make certain assumptions because other factors like population can play an important role. 

# Recommendations:

According to my model and the graphs above some of the best predictors for pointing out the status of the wells are:
1. The status of the quantity. How much a well has can help predict if it's functional. Dry wells tend to have more non functional wells, whereas enough has the most functional well of the bunch.

2. Location: The zones that are near a body of water seems to have the most functional wells, along with the most wells installed. 


```python

```
