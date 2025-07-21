_50five.json_

This is the Node Red flow

* Import the file into Node Red
* Add environment variables in Settings > Environment:
  * LOGIN_USERNAME
  * LOGIN_PASSWORD
  <img width="268" height="550" alt="image" src="https://github.com/user-attachments/assets/d93fde43-ba1e-4561-8c05-14fb0fb1b61c" />
  <img width="710" height="332" alt="image" src="https://github.com/user-attachments/assets/21f6aa6c-56b9-4469-8d6f-2fa6f8d02417" />
* Publish the flow

Current version only logs in and gets some basic information, nothing fancy yet...

<img width="1462" height="931" alt="image" src="https://github.com/user-attachments/assets/b8f57480-cd44-4af4-a0c5-a82b2453e18e" /><br>



_50five.postman_collection.json_

This is my (anonimized) json collection. API connection doesn't work but the others do...

Make sure to replace:
* &lt;USERNAME HERE&gt; = your 50five username
* &lt;PASSWORD HERE&gt; = your 50five password
* &lt;CHARGESPOT HERE&gt; = the chargespot ID returned by EndUserRechargeSpotListView_99
* &lt;NAME HERE&gt; = a name that is used to search for customers in your chargespot (my first name in my case)
* &lt;CUSTOMERID HERE&gt; = the customer id returned by RechargeSpotDashboard_642
* &lt;CARDID HERE&gt; = the card id returned by RechargeSpotDashboard_688
