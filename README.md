# Problem

## 1. Background (assumed)
In order to build a modern, friendly and energy-saving University, HCM University of Technology are delivered to the Faculty of Computer Science and Engineering the research and deployment of a system monitoring activities of students in the buildings and including measurement devices such as temperature, humidity, light in the classrooms in order to reduce energy costs. The system was piloted in the building H6 of the campus 2. In order to better service for the operation of the system, the Faculty need new design and deployment of the network in this building. The group of students studying computer networks course are invited to counsel and offer solutions to the appropriate requirements of the current building.

## 2. Detailed description
Note:
- Some information in the description below is estimates. Some
anonymous assumptions, do not exist in reality but are included in the requirements to match the target of an assignment. When deployed, the group can also make assumptions necessary to complete your design ideas.

- Encourage groups get actual data from building H6.
In campus 2, H6 building will implement a system of surveillance cameras at some point and the camera's data will be stored centrally in a server room 106 H6. There are also computer rooms on the floors 6 and 7.

To cater for monitoring, the University will invest in every classroom in the building H6 IoT devices include: 6 temperature sensors, 6 light sensors for large theory rooms (an area larger than 60 m2), the light control equipment; 3 temperature sensors, 3 light sensors for the remaining rooms (the smaller area of 60 m2), light control equipment. At each operating spread in each floor will be fitted 4 surveillance cameras. In the classrooms will be equipped with desktop computers. In practice, the computer room will be fitted with air conditioner equipment control. The measurement device will collect data continuously every 1 minute in real time and send to processing server every 5 minutes.

Description of data: A sensor will measure a different index but their data format size is 32 Kb. Sensors will collect data one-minute once and after 5 minutes they send this data to the central server over the WIFI network. The operation system of 24/7 surveillance cameras will store the data directly to a central server with a data transfer rate of 100 Mbps. The computers in the classrooms will download about 200MB per day (peak hours are 7:00 to 17:30). Each device when connected to WIFI network is used with 256 Kbps maximum speed in terms of time 7h30 to 17h30.

Also, the building H6 has an administrative office with 10 computers. The computers download about 200MB per day (peak hours are 8:00 am to 11:40 pm, 13h to 16h30) and send 10 emails per day with a maximum capacity of 10 MB per email.

In addition, each floor is the VLAN config and the system can connect to H6.


## 3. Request
The Consultants will provide specific design that the construction people can rely on it to implement the building H6. To convince the investors to choose their solutions, the consultants should also analyze the data in order to demonstrate the reasonableness of solutions. Specifically:
- Network architecture of the system in the building H6 and the IP settings for this network.
- Based on architecture above, calculate the division of subnets for each target device or divided by departments.
- Capacity needed to ensure the system operates efficiently
- The system of switches, routers and cost estimates
- Line speed internet connections
