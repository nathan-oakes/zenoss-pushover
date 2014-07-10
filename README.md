zenoss-pushover
===============

Zenoss Pushover Notifications

In Zenoss:

Install cURL and its dependencies on the machine running Zenoss (if not installed already)

sudo yum install curl

Log into your Zenoss Console
Click on the Events tab
Click on the Event Manager sub-tab
Click on the Commands link on the left panel
Add a new command by entering the name “Pushover” and then click the Add button

Click on the “Pushover” command to view the command details
Enable the command by selecting “True” for the label titled “Enabled”
Copy and paste the following into the field labeled “Command”:

curl -s \
  -F "token=APP_TOKEN" \
  -F "user=USER_KEY" \
  -F "message=hello world" \
  https://api.pushover.net/1/messages.json

Copy and paste the following into the field labeled “Clear Command”:

curl -s \
  -F "token=APP_TOKEN" \
  -F "user=USER_KEY" \
  -F "message=hello world" \
  https://api.pushover.net/1/messages.json

Click on the “Save” button at the bottom to save the changes

