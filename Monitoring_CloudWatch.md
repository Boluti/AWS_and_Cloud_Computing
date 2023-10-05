## Creating a dashboard

- In the instance you have created, scroll down to find the monitoring tab
- Click on the tab, and select manage detailed monitoring. Here we want to enable detailed monitoring so we can get monitoring data in smaller time periods:
![img_26](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/616e2411-424e-4e22-8e25-39e858a85d14)


- Once we have enabled monitoring we now need to add the charts to our dashboard. Select Add to Dashboard and a new window will open.

- In here click Create New and enter a name for a new dashboard, then hit Create. Now a dashboard has been created, it will be automatically selected and all we have to do is select add to the dashboard.
![img_28](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/a2cd1b86-8b0d-4642-9846-ba5c5e5355f4)
- We have now successfully set up a dashboard where we can monitor various metrics of our instance

![img_30](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/a04bbc8f-1ae9-4895-b58a-e74f36c949d1)


## CPU Usage alarm
While on the dashboard, select the three dots that appear by the CPU utilization chart and press view in metrics. You should see a label, copy the label as we will use this for our alarm
![img_33](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/3ba451df-25f2-4dd2-98c1-b596c222f793)

- On the left side panel ( you may need to press on the three lines) choose Alarms, then all alarms.

- Press create alarm. Select metric and enter the label ID in the search column. Find and select the CPU utilization
- Now we must set up the thresholds. Enter what you wish but I will set it as the following:


- Next, we need to create a new topic. This will store the data about where the notification will be sent. Once you have created the topic, it is automatically selected. On the next page, we will be asked to give the alarm a name and description, and after that, the alarm will be created.
![img_34](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/df06d69a-bafa-49b9-a086-be7e6e88e3e2)

- We have now created an alarm that will notify us if the CPU usage exceeds 15%:
![img_36](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/30fdd80d-263f-48a1-85e1-aab0540716f1)
![img_37](https://github.com/Boluti/AWS_and_Cloud_Computing/assets/145682024/43daae86-ace4-491a-809a-491e97656b5b)

