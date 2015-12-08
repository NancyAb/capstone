# Capstone Projects

## 1 Agrobotix

I have recieved two days of telemetry logs with about 100,000 lines. These logs correspond to
two image quality values. The goal is to be able to use the log to predict quality values.
Currently this is done by a person looking at the image with a one day turnaround to the
ground team. Agribotix has let me know that the telemtry radio signal strength to flight below 80%
may result in trouble with processing.

I have imported the data into mongo and also into a wide - 269 - dataframe on Pandas.

The data are about 80% sparse as each row is a hundreth of a second record and not all 
times have all variables.

GOALS -> Predict picture quality on-site

APPROACH -> Laptop Python code to read current log on-site and use model to predict results

PROFILE   -> Import data into MongoDB as a 'collection'
                     Export structured data for profiling - data elements, density, variance
                     Visually inspect geo / yaw / pitch/ roll elements with Tableau graphics
                     Visually inspect and question outliers

             Hypothesis test to see if mean or variance is different between groups to narrow
             down factors

 ANALYSIS ->Hold out 25% of data for testing validation of model.
                    Balance quality responses as uniform distribuion 
                     Use time series variable slope as potential factors
                     Use feature standard deviation as potential factors
                     Normalize features
                     First pass with random forest
                               - large feature count
                               - small number of observations
                     Lasso regularization
                               - interpretable results
                               - feature importance
                     k-fold validation for prediction accuracy
                     Gradient boost to improve prediction


Count | Event | Name   | p |   t
----- | ----- | ------ |  --- | ---
0|VFR_HUD|airspeed|16.3|0.0
1|VFR_HUD|groundspeed|16.3|0.0
2|VFR_HUD|heading|4.94|0.0
3|VFR_HUD|throttle|-10.5|0.0
4|VFR_HUD|alt|-3.25|0.0
5|VFR_HUD|climb|-4.33|0.0
0|AHRS2|roll|-1.71|0.087
1|AHRS2|pitch|-1.34|0.18
2|AHRS2|yaw|-19.8|0.0
3|AHRS2|altitude|-186.1|0.0
4|AHRS2|lat|194,461|0.0
5|AHRS2|lng|234,582|0.0
0|RADIO_STATUS|rssi|105.69|0.0
1|RADIO_STATUS|remrssi|-57.85|0.0
2|RADIO_STATUS|txbuf|11,244.|0.0
3|RADIO_STATUS|noise|238.8|0.0
4|RADIO_STATUS|remnoise|158.06|0.0
5|RADIO_STATUS|rxerrors|9.87|0.0
6|RADIO_STATUS|fixed|34.47|0.0
0|POWER_STATUS|Vcc|85.57|0.00
1|POWER_STATUS|Vservo|110.89|0.00
2|POWER_STATUS|flags|-inf|0.00
0|NAV_CONTROLLER_OUTPUT|nav_roll|-1.23|0.217
1|NAV_CONTROLLER_OUTPUT|nav_pitch|-5.18|0.0
2|NAV_CONTROLLER_OUTPUT|nav_bearing|14.6|0.0
3|NAV_CONTROLLER_OUTPUT|target_bearing|-14.7|0.0
4|NAV_CONTROLLER_OUTPUT|wp_dist|6.79|0.0
5|NAV_CONTROLLER_OUTPUT|alt_error|-9.55|0.0
6|NAV_CONTROLLER_OUTPUT|aspd_error|NaN|NaN
7|NAV_CONTROLLER_OUTPUT|xtrack_error|NaN|NaN
0|SCALED_PRESSURE|time_boot_ms|-15.2|0.0
1|SCALED_PRESSURE|press_abs|221.3|0.00
2|SCALED_PRESSURE|press_diff|7.30|0.0
3|SCALED_PRESSURE|temperature|3.74|0.0

DETAILS -> Sample log rows:

2015-09-15 12:20:43.22: HEARTBEAT {type : 6, autopilot : 8, base_mode : 0, custom_mode : 0, system_status : 0, mavlink_version : 3}
2015-09-15 12:20:43.23: TERRAIN_REPORT {lat : 451473107, lon : -729875865, spacing : 100, terrain_height : 57.573261261, current_height : 0.304172813892, pending : 0, loaded : 336}

## 2 Google Analytics www.animalacupressure.com 

data mining google analytics results
supervised and unsupervised data
recommendation engine if data is sparse?
capture user attributes for recommendation system
find out dimensions and number of rows of sample data
Data is not aggregated.

question using data?
website google analytics for seo
facebook
click through rates
analalytics google
session
tallgrasspublishers
holland computers
learn power online course
google --
first of december review.

## 3 mimi database with nursing home data

gartner third party data that is clean with nursing home search
results. categorical nursing home recommender along different
attributes e.g. according to price, proximity to urban area,
different types of outcomes.
potential unsupervised data analysis.



