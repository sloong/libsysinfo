# Lightweight Linux Monitoring Library
For several Projects on Raspberry Pi or OrangePi or my Mini Server i wanted to Monitor the System Load, so therefore, 
i created this Library where i can get the CPU Load / Ethernet Load and Memory consumption, to send it via Websocket to 
a backend application or print it on a display. 


[Picture of LCD with load].


[Screenshot of Grafana and Load].



### Features:

* CPU Usage:
  * total CPU Usage
  * CPU Usage per Core
  * CPU Information
    
* Networkinterface load:
  * Bytes/Bits per Second
  * Total Received or Transmitted Bytes

* Memory Usage:
  * System Memory Usage
  * Total Memory
  * Memory Usage per Process
  
### Monitorig Data are presented in JSON: 
therefore the most popular [C++ JSON lib](https://github.com/nlohmann/json) + the very cool [Json to C++](https://app.quicktype.io/) Code 
    
    {
      "Linuxsystemmonitoring": {
        "linuxethernet": [
          {
            "iFace": "eth0",
            "BitsRXSecond": "undef",
            "BytesRXSecond": "89Byte/s",
            "BytesRXTotal": 92824691,
            "BytesTXSecond": "22Byte/s",
            "BytesTXTotal": 5783311275,
            "BytesTotal": 5876135966,
            "BytesTotalPerSecond": "97Byte/s"
          }
        ],
        "MemoryUsage:": {
          "MemoryUsage_KIB": 11195216,
          "MemoryUsage_perc": 34.0,
          "MemoryUsage_totalKIB": 32893064,
          "MemoryUsage_of_process:": 349822
        },
        "CPU": {
          "CPUUsage": 7.99,
          "CPU_Type": "Intel I7",
          "num_of_cores": 12,
          "MultiCore": [
            "CPU0:4.85%",
            "CPU1:7.77%",
            "CPU2:11.76%",
            "CPU3:9.52%",
            "CPU4:4.04%",
            "CPU5:1.98%",
            "CPU6:6.86%",
            "CPU7:4.90%",
            "CPU8:15.69%",
            "CPU9:5.05%",
            "CPU10:17.48%",
            "CPU11:7.92%",
            "CPU12:9.90%",
            "CPU13:9.52%",
            "CPU14:7.92%",
            "CPU15:9.71%"
          ],
          "MultiUsage": [
            4.85,
            7.77,
            11.76,
            9.52,
            4.04,
            1.98,
            6.86,
            4.9,
            15.69,
            5.05,
            17.48,
            7.92,
            9.9,
            9.52,
            7.92,
            9.71
          ]
        },
        "system": {
          "SysUptime": 37008,
          "SysUptime_days": 0,
          "SysUptime_hours": 10,
          "SysUptime_min": 16,
          "SysUptime_sec": 48
        }
      },
      "type": "system"
    }
 
  
  

* Linux Features:
    * is remote Device Online - (parse Ping response)
    * getPID by Name
    * getOSVersion
    * SysUptime
    * Number of Threads by PID 
    * setApplication as Deamon


## How to build:

## Example:

## Todo:
* CPU Usage per Process
* example -> monitoring and creating graph with grafana
* Testing: Catch2 tests
* Data Export in JSON, BSON,MSGPack, XML
* logging and average of 30min, 2h, 6h, 24h , 2d, 7d. 
* Documentation

# Get in Contact: 
If there are any Bugs or Request for extensions or features, feel free
[email me](fuxeysolution@gmail.com) me or [buy me a coffee](https://www.paypal.me/fuxeey).



