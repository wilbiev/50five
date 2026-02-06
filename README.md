# This is the Node Red flow for 50five charging station - version 2.1

* Import the file into Node Red
* Change the URL, username and password on the subflow
* Publish the flow

## Current flow 50five_v2.1.json supports:
* Login
* Start/Stop charging
* Poll status
* Hard/Soft reset
* Unlock connector
* Block/Unblock charging
* Logout
* Use MQTT to send actions
* Use MQTT to receive status
* Creates home assistant buttons, select, sensors & switch

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
* 50five Connector
  * Attributes: Spot idx, Channel ID, Card idx, Customer idx, Customer name, Customer address, Cost center, Software version

* 50five Status
  * Attributes: Data (transaction log information)

## Home Assistant select:
* 50five Card-ID (select your charging card)

## Home Assistant switch:
* 50five Charging switch (switch to start/stop charging)


## Thanks
Special thanks to [dgthomson](https://github.com/dgthomson/nodered-shellrecharge) for his Shell Recharge script!!

Special thanks to [nikagl](https://github.com/nikagl/50five) for the first version of this script!!