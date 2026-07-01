# Practical Session: Farewell to MbedOS

## Introduction to Real Time Operating Systems, LoRaWAN and The Things Network.
In this practical session we will look into what Realtime operating systems (RTOS) are and the benefits. Also, we will utilize the Mbed platform to program a microcontroller on a test board and get some data. For data transmission we will utilize the LoRaWAN and the test board will be registered on The Things Network (TTN). From TTN we will utilize NodeRed to transfer data from a TTN application to an Influx timeseries database for permanent storage.

### Requirements for the Interactive Sessions 
Please download and install this tools.
1. Download and install *Tera Term*. Link: **[TeraTerm Link](https://github.com/DeKUT-DSAIL/Minds_Machines_and_Matrices_2026/blob/main/Introduction%20to%20Embedded%20Systems%20and%20IoT/assets/teraterm-4.92.exe)**.
2. Download Influxdb zip folder from the following link. Link: **[InfluxDB](https://dl.influxdata.com/influxdb/releases/v1.12.4/influxdb-1.12.4-windows_amd64.zip)**.
    - Create a desktop folder - `influx`
    - Unzip the downloaded zip into this folder
    - To check whether the download is working, double click the `influxd.exe` and leave it running 
    - Using your command prompt, navigate into the influx folder with all the contents and run `influx.exe`
    - Next command `show databases`
    - The output should be similar to Figure 1.
    | ![influx1](/img/influx1.png) | 
    |:--:| 
    | *Figure 1: Influx Output 1* |
    - To create a database for the session run `create database outreach_2026`
    - Run `show databases` again to check whether the database was created.

