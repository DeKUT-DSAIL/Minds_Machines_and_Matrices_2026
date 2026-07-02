# Practical Session: Farewell to MbedOS

##  LoRaWAN and The Things Network.
In this practical session we will look into what Realtime operating systems (RTOS) are and the benefits. Also, we will utilize the Mbed platform to program a microcontroller on a test board and get some data. For data transmission we will utilize the LoRaWAN and the test board will be registered on The Things Network (TTN). From TTN we will utilize NodeRed to transfer data from a TTN application to an Influx timeseries database for permanent storage.

### Requirements for the Interactive Sessions 
Please download and install these tools.

1. Download and install *Tera Term*. Link: **[TeraTerm Link](https://github.com/DeKUT-DSAIL/Minds_Machines_and_Matrices_2026/blob/main/Introduction%20to%20Embedded%20Systems%20and%20IoT/assets/teraterm-4.92.exe)**.
2. Download *Influxdb zip folder* from the following link. Link: **[InfluxDB](https://dl.influxdata.com/influxdb/releases/v1.12.4/influxdb-1.12.4-windows_amd64.zip)**.
    - Create a desktop folder - `influx`
    - Unzip the downloaded zip into this folder
    - To check whether the download is working, double click the `influxd.exe` and leave it running 
    - Using your command prompt, navigate into the influx folder with all the contents and run `influx.exe`
    - Next command `show databases`
    - The output should be similar to Figure 1.

    | ![influx1](img/influx1.png) | 
    |:--:| 
    | *Figure 1: Influx Output 1* |

    - To create a database for the session run `create database outreach_2026`
    - Run `show databases` again to check whether the database was created.
3. Download and Install *NodeRed* using the following steps.
    - Install `Node.js` - Download the latest LTS version of Node.js from the official Node.js home page. Link: **[Node](https://nodejs.org/dist/v24.18.0/node-v24.18.0-x64.msi)**.
    - Run the downloaded MSI file
    - Once installed, open a command prompt and run the following command to ensure *Node.js* and *npm* are installed correctly. Command: `node --version && npm --version`
    - Thwe output should as shown on Figure 2.

    | ![node1](img/node1.png) | 
    |:--:| 
    | *Figure 2: NodeRed Output* |

    - Install Node-RED: Run the following command: `npm install -g node-red`
    - To run Node-RED: `node-red`
    - The output should be as shown on Figure 3.

    | ![node2](img/node2.png) | 
    |:--:| 
    | *Figure 3: NodeRed Output when running* |

    - To use NodeRed, run the local server link on your favourite browser: `http://127.0.0.1:1880`
    - Figure 4, shows the output.

    | ![node3](img/node3.png) | 
    |:--:| 
    | *Figure 4: NodeRed Terminal* |

Please create accounts for the following.
1. **The Things Network**
     An IoT (Internet of Things) system can be broadly divided into 3 main layers. The first layer is the perception layer which includes sensors and actuators involved in data collection. The second layer is the network layer which is responsible for communication between devices in the system. The network layer includes elements such as gateways and network servers. The last layer is the application layer, where an end user gets to interact with data output.
     The network server under the network layer is a crucial component in a deployment scenario. The network server is a central element and is in charge of management of gateways, the authorization of end nodes and the exchange of data (uplink and downlink) between the sensor node and the user application.
     The Things Network is a free LoRaWAN network server that is open to all. It has popularized the LoRaWAN technology by offering free services to IoT enthusiasts especially during initial tests before professional deployments.

     To open a TTN account we are going to follow the steps in following link: Link: **[The Things Network Account](https://dekut-dsail.github.io/tutorials/tutorial-water-resource/tp2.html)**.
2. **ARM Keil Studio**
    Keil Studio Cloud is a web based IDE that allows for the creation, running and debugging of embedded applications. It runs ARM Mbed OS which is an open source operating system for microcontrollers. It is a great tool for beginners as it does not require any installation and is very easy to use.

    To Open an account click on the following link select the `classic` option and move on from there: Link **[ARM Keil Studio](https://studio.keil.arm.com/auth/login)**.


