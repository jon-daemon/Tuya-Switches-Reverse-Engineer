# Tuya-Switches-Reverse-Engineer

## Connections

*Not all connectors on every variation*
#### Front PCB

**6 pads pinout**

| 3V3 | ESP P25/Rx | ESP P26/Tx | ESP P15/IO0 | ESP P31/RST | GND |
| --- | ---------- | ---------- | ----------- | ----------- | --- |

#### Back PCB

**6 Pins Connector**

| Relay 3 | Relay 2 | Relay 1 |
| ------- | ------- | ------- |
| 3V3     | GND     | 3V3     |

## Photos

### 1 Sensor

*Tuya version 1.1.1*

<p align="center">
<img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/4e3e3e35-6e21-44a9-9f3c-895540532dfe" width="30%">
</p>

#### SMATRUL
<p align="center">
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/2f851109-3fe2-42a8-a9bf-ba197ecfd3a6" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/e93dc688-188f-4d3d-b434-bcdc76662c73" width="30%">
</p>

#### WIFI-W3C

<p align="center">
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/85c56059-fc4f-4877-9a64-f6a63b62364f" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/963a644a-02ae-440f-8c20-77edb33e3248" width="30%">
</p>

### 2 Sensors

*Tuya version 1.1.2*

<p align="center">
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/63fb4b09-441d-4a4a-b5ac-2cac11a5c548" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/f06f6b08-42a1-4084-8673-64b9eae205cf" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/530156da-1ef9-4171-ac1e-4ec35045982b" width="30%">
</p>

### 3 Sensors

*Tuya version 1.1.2*

<p align="center">
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/ed1d38a0-0241-4f83-bc12-57b17419c8ee" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/29c25c58-cc50-4cd8-ba68-90a5fb27b603" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/245c5cbc-a715-49a2-84a7-98d7fb56b611" width="30%">
</p>

### 4 Sensors

*Tuya version 1.1.8*

<p align="center">
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/d38e5c2e-9d4f-450b-a652-330224084fd6" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/c6b29006-cf39-4ab0-b572-76c3ff5a6db2" width="30%">
&nbsp; &nbsp; 
  <img src="https://github.com/jon-daemon/Tuya-Switches-Reverse-Engineer/assets/206048/7e0c0b08-9c03-4827-ad31-f13ce676b30d" width="30%">
</p>

# Pinouts
#### 1/2/3 Gangs

**(haven't tested 4 gangs!)**

*the first two columns are the pins of the unknown chip*

| SMATRUL | W6C | 1/2/3 Sensors        |                                 |                                     |
| ------- | --- | -------------------- | ------------------------------- | ----------------------------------- |
| 1       |     | buzzer               |                                 |                                     |
| 2       |     | 4 pads connector (2) |                                 |                                     |
| 3       |     | 4 pads connector (3) |                                 |                                     |
| 4       | 12  | ESP P24/IO5          |                                 | sends touch Middle signal           |
| 5       | 11  | ESP P25/IO3/Rx       | *unsolder for UART flash*       | sends touch Left signal             |
| 6       |     | 4K7 -- > ESP P26/IO1 | -- > 1K -- > status LED cathode |                                     |
|         |     | 1K -- > PNP? base    | collector -- > BLUE LEDs anode  |                                     |
| 7       |     |                      |                                 |                                     |
| 8       | 16  | Touch  1             |                                 | reads touch Left signal             |
| 9       | 1   | Touch  2             |                                 | reads touch Middle signal           |
| 10      | 2   | Touch  3             |                                 | reads touch Right signal            |
| 11      | 15  | ESP P16/IO4          |                                 | sends touch Right signal            |
| 12      |     | ESP P12/IO13         | Relay 1 (Left touch)            | LED Left BLUE cathode / RED anode   |
| 13      |     | ESP P10/IO12         | Relay 2 (Middle touch)          | LED Middle BLUE cathode / RED anode |
| 14      |     | ESP P9/IO14          | Relay 3 (Right touch)           | LED Right BLUE cathode / RED anode  |
| 15      |     |                      |                                 |                                     |
| 16      |     | GND                  |                                 |                                     |
