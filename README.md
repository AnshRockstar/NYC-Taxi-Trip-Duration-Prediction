#NYC_taxi price predication

The dataset is based on the 2016 NYC Yellow Cab trip record data made available in Big Query on Google Cloud Platform. The data was originally published by the NYC Taxi and Limousine Commission (TLC). The data was sampled and cleaned for the purposes of this playground. Based on individual trip attributes, should predict the duration of each trip.

Source:
Download Data : https://drive.google.com/drive/u/0/folders/1_hRIm4eP47rVfOK1kGTMp2Y12UVC3JXj

Details:
File descriptions :

● NYC Taxi Data.csv - the dataset (contains 1458644 trip records)

Data fields
● id - a unique identifier for each trip

● vendor_id - a code indicating the provider associated with the trip record

● pickup_datetime - date and time when the meter was engaged

● dropoff_datetime - date and time when the meter was disengaged

● passenger_count - the number of passengers in the vehicle (driver entered value)

● pickup_longitude - the longitude where the meter was engaged

● pickup_latitude - the latitude where the meter was engaged

● dropoff_longitude - the longitude where the meter was disengaged

● dropoff_latitude - the latitude where the meter was disengaged

● store_and_fwd_flag - This flag indicates whether the trip record was held in vehicle memory before sending to the vendor because the vehicle did not have a connection to the server - Y=store and forward; N=not a store and forward trip

● trip_duration - duration of the trip in seconds

Objective:
Build a model that predicts the total trip duration of taxi trips in New York City.
