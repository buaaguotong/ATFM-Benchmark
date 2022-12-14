## Brief Description of the ATFM Benchmark

This air traffic flow management (ATFM) benchmark consists of eight national-wide instances, which are extracted from Chinese domestic airspace during different period.

Each instance is named as ''MM-DD-AM/PM''. The running period covers morning (AM, 9:00--12:00) and afternoon (PM, 15:00--18:00), weekday and weekend. Their basic information is shown in the following table. Each instance consists of around 900+ scheduled aircraft, 180+ airports, 2000+ available air routes. 

![map](D:\TEVC修改\数据公开\img\map.png)

![data_info](D:\TEVC修改\数据公开\img\data_info.png)





## How to Use the Instance?

For each instance, there are three data files, i.e., **flight_data. xls**, **default_speed.npy**,  **path_length.npy**.

* **flight_data.xls**: this data file can be visited using Excel. Each row represents a flight schedule of one aircraft, which includes the location of origin/destination airports (given in longitude and latitude), planned take-off/arrival timeslot (given in minutes), available route number, and the location of waypoints on each air route. Given a flight plan, including the departure time, selected air routes, and the speed profiles on the selected routes, then, the potential conflicts and delays induced by the flight plan can be calculated.
* **default_speed.npy:** this data file can be loaded by numpy. It is a 2-D array, where the row represents the aircraft index, the column denotes its default speed values on each air route segment (given in kilometer per second).
* **path_length.npy:** this data file can be loaded by numpy. It is also a 2-D array, where the row represents the aircraft index, the column denotes the length of each air route (given in kilometer). 