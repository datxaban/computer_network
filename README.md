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

# Propose solution

## 1. Overall Structure:
- **Floor**:
    - **Floor 1**: Has 1 Administrative office, and may have some people come
across with their own devices because this is the ground floor
    - **Floor 2-4**: Has 4 small rooms, 2 large rooms
    - **Floor 5**: Has 1 laboratory (large room), 1 large room, 4 small rooms
- **Room**: 
    - **Laboratory**: Has 30 computers
    - **Administrative office**: Has 10 computers, and 20 people with 40 devices
    - **Small room**: Has capacity for maximum 30 people with 60 devices
    - **Large room**: Has capacity for maximum 60 people with 120 devices
- **Equipment**:
    - **Sensor**: Temperature sensors and light sensors collect data one time per
    minute and after 5 minutes they will send this to central server. The
    common data format size is fixed at 32Kb
    - **Camera**: Surveillance cameras operate 24/7 and store data directly to server
    with transfer rate of 100Mbps
    - **Wifi**: Allocate data transfer rate for each connected device maximum 256
    Kbps in 7:30AM – 5:30PM
    - **Administrative office**: Desktop computers which can download 200MB
    per day and send 10 emails per day with a maximum capacity of 10MB per
    email.
    - **Other rooms**: Desktop computers can download 200MB per day
## 2. Network Traffic
- **Device**: Assume in the peak hour, all people (included in the classroom and the
hall) are using internet devices, each small room has maximum 60 devices and
we have 4 small rooms for each floor, and 4 floors in total. For floor 1, there
are 20 devices in the office and maximum 60 devices in the hall.
Total: (120*2 + 60*4) *4 + 20 + 60 = 2000 devices, each device has maximum
256 Kbps transmission rate and it’s reduced half in peak hour, so
2000*128(Kbps) = 256 Mbps.
- **Computers**: lab room has 30 computers, office 10 has computers, and the rest
have only 1 computer.
Total: 30 + 10 + 5 + 6*3 = 63 each one download 200 MB a day and average
all pc need 5.72 Mbps traffic.
- **Sum up: 261.72 Mbps**
## 3. Storage Capacity
- **Sensor**: each floor has 48 sensors except floor 1 has 12 sensors. Total 48*4 + 12 = 204 sensor -> 1880 Mb a day.
- **Camera system**: 100 Mbps -> 8640000 Mb a day. Total: 1080 GB a day.
## 4. Physical Design
![Physical Design](/assets/physical.png "Physical Design")


## 5. Logical diagram
![Logical Design](/assets/logical.png "Logical Design")

## 6. Equipment list used and expected cost:
| Product               | Type | Number   |
| :---                  |    :----              | ---: |
| TP-LINK TL-SG5412F    | Switch 12-Port        | 1    |
| TP-LINK TL-SF1008D    | Switch 8-Port         | 5    |
| TP-LINK T3700G-28TQ   | Switch 12-Port        | 1    |
| J-tech AHD VP-102AHDH | Camera                | 100  |
| Intel Xeon E5-2609v3(1.9GHz/6-core/15MB/85W) + <br> Ram 32GB + mouse, keyboard   | Server + HardDisk(300TB) + Gears                         | 1    |
| Fortigate 60D         | Firewall              | 1    |
| 42U D1100 MICA        | Rack Cabinet          | 1    |
| UTP CAT5              | Cable                 | 1000m| 
| THERMASGARD®RTF1 SD LM235Z   | Thermal Sensor | 102  |
| LS6B                  | Light Sensor          | 102  |
|  Grandstream GWN7600  | Access point          | 3    |
| Fiber300Eco+(300Mbps) |                       |      |

- Total cost for 5 years: 863,489,330 vnd

## 7. Advantages
- HD Camera
- Sensitive sensor system
- Fexible network design
- Server’s high security with firewall
- High harddisk capacity: up to 1 year (284 days)
## 8. Disadvantages
- High price
- Complex system of IOT devices