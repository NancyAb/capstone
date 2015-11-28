# Capstone Projects

## 1 Agrobotix

run python code on tlog and check results
404 observations
check features and quality match.
need to know how to merge data

telemtry radio signal strength to flight below 80%
trouble with processing

automation of classifaction

real time classification tlog results for image quality

check for normalization of dependent variable!!



GOALS -> Predict picture quality on-site

APPROACH -> Laptop Python code to read current log on-site and use model to predict results

PROFILE   -> Import data into MongoDB as a 'collection"
                     Export structured data for profiling - data elements, density, variance
                     Visually inspect geo / yaw / pitch/ roll elements with Tableau graphics
                     Visually inspect and question outliers

             Hypothesis test to see if mean or variance is different between groups to narrow
             down factors

 ANALYSIS ->Hold out 25% of data for testing validation of model.
                     Normalize features
                     First pass with random forest
                               - large feature count
                               - small number of observations
                     Lasso regularization
                               - interpretable results
                               - feature importance
                     k-fold validation for prediction accuracy

DETAILS ->
mongodb data collection of all 401 missions
collection contains documents with embedded sub-documents:

-> mission id document
    -> event id with timestamp sub-document (e.g. 2015-09-12 12:35:57.61:.0.0) timestamp is not unique so need additional id
          -> drone event e.g. (NAV_CONTROLLER_OUTPUT, FENCE_STATUS, GLOBAL_POSITION_INT)
               -> drone event details (e.g. {nav_roll : 0.0, nav_pitch : 0.0, nav_bearing : 68, target_bearing : 90, wp_dist : 0, alt_error : 0.0, aspd_error : 0.0, xtr})




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



