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
                     Use time series variable slop as potential factors
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

DETAILS -> Sample log rows:

2015-09-15 12:20:43.22: HEARTBEAT {type : 6, autopilot : 8, base_mode : 0, custom_mode : 0, system_status : 0, mavlink_version : 3}
2015-09-15 12:20:43.23: TERRAIN_REPORT {lat : 451473107, lon : -729875865, spacing : 100, terrain_height : 57.573261261, current_height : 0.304172813892, pending : 0, loaded : 336}

n [62]: sign_df.head(34)
Out[62]: 
                   event             name             p              t
0                VFR_HUD         airspeed  1.634296e+01   4.520671e-59
1                VFR_HUD      groundspeed  1.634296e+01   4.520671e-59
2                VFR_HUD          heading  4.943246e+00   7.841505e-07
3                VFR_HUD         throttle -1.045811e+01   1.971107e-25
4                VFR_HUD              alt -3.249225e+00   1.162042e-03
5                VFR_HUD            climb -4.334992e+00   1.475737e-05
0                  AHRS2             roll -1.708932e+00   8.750321e-02
1                  AHRS2            pitch -1.343402e+00   1.791809e-01
2                  AHRS2              yaw -1.975936e+01   7.676690e-85
3                  AHRS2         altitude -1.861437e+02   0.000000e+00
4                  AHRS2              lat  1.944619e+05   0.000000e+00
5                  AHRS2              lng  2.345821e+05   0.000000e+00
0           RADIO_STATUS             rssi  1.056901e+02   0.000000e+00
1           RADIO_STATUS          remrssi -5.784640e+01   0.000000e+00
2           RADIO_STATUS            txbuf  1.124426e+04   0.000000e+00
3           RADIO_STATUS            noise  2.388205e+02   0.000000e+00
4           RADIO_STATUS         remnoise  1.580630e+02   0.000000e+00
5           RADIO_STATUS         rxerrors  9.868131e+00   1.719776e-22
6           RADIO_STATUS            fixed  3.446963e+01  2.267390e-207
0           POWER_STATUS              Vcc  8.557281e+01   0.000000e+00
1           POWER_STATUS           Vservo  1.108861e+02   0.000000e+00
2           POWER_STATUS            flags          -inf   0.000000e+00
0  NAV_CONTROLLER_OUTPUT         nav_roll -1.234655e+00   2.170347e-01
1  NAV_CONTROLLER_OUTPUT        nav_pitch -5.186442e+00   2.254226e-07
2  NAV_CONTROLLER_OUTPUT      nav_bearing  1.467054e+01   1.877408e-47
3  NAV_CONTROLLER_OUTPUT   target_bearing -1.472891e+01   8.301754e-48
4  NAV_CONTROLLER_OUTPUT          wp_dist  6.790601e+00   1.288800e-11
5  NAV_CONTROLLER_OUTPUT        alt_error -9.551494e+00   2.205912e-21
6  NAV_CONTROLLER_OUTPUT       aspd_error           NaN            NaN
7  NAV_CONTROLLER_OUTPUT     xtrack_error           NaN            NaN
0        SCALED_PRESSURE     time_boot_ms -1.521307e+01   2.648532e-50
1        SCALED_PRESSURE        press_abs  2.212826e+02   0.000000e+00
2        SCALED_PRESSURE       press_diff  7.301807e+00   3.669659e-13
3        SCALED_PRESSURE      temperature  3.743108e+00   1.853637e-04



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



