# This is the Node Red flow for 50five charging station.

* Import the file into Node Red
* Change the URL, username and password on the subflow
* Publish the flow

## Current flow 50five_v2.0.json supports:
* Login
* Start/Stop charging
* Poll status
* Hard/Soft reset
* Unlock connector
* Block/Unblock charging
* Logout
* Use MQTT to send actions
* Use MQTT to receive status
* Creates home assistant buttons & switch for start/stop

## Home Assistant buttons:
* 50five Start
* 50five Stop
* 50five Poll
* 50five Soft reset
* 50five Hard reset
* 50five Unlock connector
* 50five Block charging
* 50five Unblock charging

## Home Assistant sensors:
* 50five Card-ID
  * Atributes: Card idx, Customer idx, Customer name, Customer address, Cost center

* 50five Connector
  * Attributes: Spot idx, Channel ID, Software version

* 50five Status
  * Attributes: Data (transaction log information)

## Home Assistant switch:
* 50five Charging switch

In the "Save cardID" change node (subflow) you may need to the payload depending on the card you'd like to use:
Default is using the first card: 
```
payload[0][0].id, payload[0][0].text
```
If you want to use the second card you can change this to:
```
payload[0][1].id, payload[0][1].text
````

## Thanks
Special thanks to [dgthomson](https://github.com/dgthomson/nodered-shellrecharge) for his Shell Recharge script!!

Special thanks to [nikagl](https://github.com/nikagl/50five) for the first version of this script!!