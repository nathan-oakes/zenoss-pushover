zenoss-pushover
===============

##Zenoss Pushover Notifications

In Zenoss:<br>

Install cURL and its dependencies on the machine running Zenoss (if not installed already)<br>

sudo yum install curl<br>

Log into your Zenoss Console<br>
Click on the Events tab<br>
Click on the Event Manager sub-tab<br>
Click on the Commands link on the left panel<br>
Add a new command by entering the name “Pushover” and then click the Add button<br>

Click on the “Pushover” command to view the command detail<br>
Enable the command by selecting “True” for the label titled “Enabled”<br>
Copy and paste the following into the field labeled “Command”:<Br>

<code>
curl -s \
  -F "token=APP_TOKEN" \
  -F "user=USER_KEY" \
  -F "message=hello world" \
  https://api.pushover.net/1/messages.json
</code>

Copy and paste the following into the field labeled “Clear Command”:
<code>
curl -s \
  -F "token=APP_TOKEN" \
  -F "user=USER_KEY" \
  -F "message=hello world" \
  https://api.pushover.net/1/messages.json
  </code>
<br>
Click on the “Save” button at the bottom to save the changes

