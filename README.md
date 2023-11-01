## Brief Description of the ATFM Benchmark

This air traffic flow management (ATFM) benchmark consists of eight national-wide instances, which are extracted from Chinese domestic airspace during different periods.
This benchmark is used as a test suite for Air Traffic Flow Management.

Note that the released data are Simplified Version of the original data. The whole original data, unfortunately, cannot be fully disclosed due to stringent data privacy concerns and confidentiality agreements in place with our data providers. These agreements strictly limit the extent of data sharing to ensure the protection of sensitive information intrinsic to air traffic operations. However, to contribute to the community, we have made a conscientious effort to share a representative subset of the data. This includes details of the basic backbone network structure, information about hub airports, and departure times that are sampled from a Poisson distribution. We believe that this subset is sufficient for understanding the context and replicating the experimental setup, while still adhering to the confidentiality constraints imposed on us.

Each instance is named as ''MM-DD-AM/PM''. The running period covers morning (AM, 9:00--12:00) and afternoon (PM, 15:00--18:00), weekday and weekend. Their basic information is shown in the following table. Each instance consists of around 900+ scheduled aircraft, 180+ airports, 2000+ available air routes. 

If you have any questions, please feel free to catact me (email:guotong1997@buaa.edu.cn)

![map](https://github.com/buaaguotong/ATFM-Benchmark/blob/main/img/map.png)

![data_info](https://github.com/buaaguotong/ATFM-Benchmark/blob/main/img/data_info.png)





## How to Use the Instance?

For each instance, there are three data files, i.e., **flight_data. xls**, **default_speed.npy**,  **path_length.npy**.

* **flight_data.xls**: this data file can be visited using Excel. Each row represents a flight schedule of one aircraft, which includes the location of origin/destination airports (given in longitude and latitude), planned take-off/arrival timeslot (given in minutes), available route number, and the location of waypoints on each air route. Given a flight plan, including the departure time, selected air routes, and the speed profiles on the selected routes, then, the potential conflicts and delays induced by the flight plan can be calculated.
* **default_speed.npy:** this data file can be loaded by numpy. It is a 2-D array, where the row represents the aircraft index, the column denotes its default speed values on each air route segment (given in kilometer per second).
* **path_length.npy:** this data file can be loaded by numpy. It is also a 2-D array, where the row represents the aircraft index, the column denotes the length of each air route (given in kilometer). 
