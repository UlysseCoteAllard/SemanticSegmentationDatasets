# SemanticSegmentationDatasets

This repository contains the EMG artificial dataset and Dance artificial dataset as presented in ...

The EMG artificial dataset is based on data from: Long Term EMG Dataset (https://github.com/UlysseCoteAllard/LongTermEMG) 

The Dance Dataset dataset is based on data from: Dance Dataset (https://doi.org/10.1145/3323213).

## Usage
The artificial datasets conists of multiple timeseries divided into train, validation and test sets. The data is represented in a csv-format where each column contains the data from one channel, except for the last column which contains the true changepoint location between the gestures/dance-moods (represented as: 0=No Changepoint, 1=Changepoint). 

The EMG artificial dataset is based on 3DC which is a ten-channel, dry electrode 3D printed EMG band with a sampling rate of 1000 Hz.

Example:
channel0,channel1,channel2,channel3,channel4,channel5,channel6,channel7,channel8,channel9,true_locs
99.0,96.0,120.0,214.0,259.0,27.0,-199.0,23.0,135.0,43.0,0.0
132.0,73.0,101.0,197.0,148.0,-107.0,-42.0,79.0,124.0,65.0,0.0
155.0,74.0,0.0,36.0,48.0,-45.0,27.0,199.0,84.0,76.0,0.0
63.0,45.0,18.0,0.0,11.0,-39.0,24.0,282.0,-1.0,-5.0,0.0
-56.0,-46.0,40.0,66.0,60.0,13.0,23.0,292.0,-75.0,-51.0,0.0

The Dance Dataset dataset is based on a nine degree of freedom IMU (inertial measurement unit). Data from the two IMU sensors are represented by yaw, pitch roll coordinates and are sampled at 50Hz.

|     | Pitch    | Yaw      | Roll     |
|-----|----------|----------|----------|
| Arm | channel0 | channel1 | channel2 |
| Leg | channel3 | channel4 | channel5 |

Example:
channel0,channel1,channel2,channel3,channel4,channel5,true_locs
-0.9045919179916382,0.5533947944641113,0.06179441139101982,2.0612730979919434,-1.3658392429351807,0.00016890247934497893,1.0
-0.9300351142883301,0.5494210124015808,0.06656480580568314,2.0994632244110107,-1.3126235008239746,-0.09445899724960327,0.0
-0.953470766544342,0.5424953103065491,0.060376137495040894,2.212841272354126,-1.2735230922698975,-0.11450131237506866,0.0
-0.9592191576957703,0.5450705289840698,0.05768774077296257,2.3154194355010986,-1.2706670761108398,-0.15026934444904327,0.0
