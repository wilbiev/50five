_50five.json_

This is the Node Red flow for 50five charging station.

* Import the file into Node Red
* Change the URL, username and password on the subflow
* Publish the flow

Current flow supports:
* Login
* Start/Stop charging
* Poll status
* Reset (softreset, not sure yet what the difference between hard- and softreset is)
* Logout
* Use MQTT to send actions
* Use MQTT to receive status
* Creates home assistant buttons & switch for start/stop/polling/reset

In the "Extract Card ID" function node you may need to replace this depending on the card you'd like to use:

```
var cardid = payload[0][1].id;
````

change this to the following if you would like to use the first card:

```
var cardid = payload[0][0].id;
````

_50five.postman_collection.json_

This is my (anonimized) json collection. API connection doesn't work but the others do...

Make sure to replace:
* &lt;USERNAME HERE&gt; = your 50five username
* &lt;PASSWORD HERE&gt; = your 50five password
* &lt;CHARGESPOT HERE&gt; = the chargespot ID returned by EndUserRechargeSpotListView_99
* &lt;NAME HERE&gt; = a name that is used to search for customers in your chargespot (my first name in my case)
* &lt;CUSTOMERID HERE&gt; = the customer id returned by RechargeSpotDashboard_642
* &lt;CARDID HERE&gt; = the card id returned by RechargeSpotDashboard_688
