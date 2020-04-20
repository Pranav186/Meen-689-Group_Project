# Meen-689-Group_Project
Group Members
Sumil Sood [329006457]
Pranav Natu [430000211]
Siddharth Sane [829009471]
Jay Shah [930001954]
Aditya Bitra [230002273]
# Kalman Filter
The data for Accelerometer and GPS was collected using the mobile phone sensors and was collected while holding the mobile still and moving in a straight line for 45 meters at a constant velocity. Although the expected path is a straight line and expected velocity is constant but there is always some disturbances and therefore the actual path is approximated using the Kalman filter.\
The file 'Kalman_filter.m' is the main file and contains all the code required to run the filter to predict states. It has few functions dependencies including:\
1. Accelero_to_position.m (required to process raw data from accelerometer)\
2. Gps_to_bodyframe.m (Required to convert the GPS data which is in global coordinate frame to the local accelerometer body frame) 
The data is collected and stored in two files named 'sensorlog_40.4m.mat' (data from IMU, GPS) and 'meen689' (data from ultrasonic sensor).\
The plots of the estimated position and velocity are shown. The results have saw like graph because the estimate tends to divert due the the noisy accelerometer measurements but is kept in check as soon as the GPS measurement comes in whose frequency is less.


# Bayesian Filter
The file 'SensorFusion.m' is the main file for Bayesian Filter.
It will require the following to run:
1)sensorlog_40.4m.mat (data from IMU, GPS)\
2)Accelero_to_position.m (Function to convert acceleration to position, velocity)\
3)Gps_to_bodyframe.m ( Function to convert GPS data to bodyframe)\
4)BayesianEstimate.m ( Function to filter by Bayesian estimate)\
Results:\
1) Position in X and Y\
2) Velocity in X and Y
