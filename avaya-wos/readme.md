# Avaya-WOS Check_MK Plugin
This check is a Check_MK Agent plugin. 
It connects to the Avaya WOS Server Appliance and is using the JSON API to retrieve some values.
Because there is no command line access to the WOS Appliance, the Check has to be installed at a different Server with a Check_MK Agent installed. I used the Check_MK server itself.
The Token for accessing the WOS API is only for 7 days valid, thus we need to generate a new one inside the script when timed out.
Actually we only retrieve two values: concurrent online WiFi users ("online") and unique users seen in last 24 hours ("unique24h").

# Installation
See instructions in script file (comments).

Short:
- install script in agent plugin script directory
- make a discovery (full scan) in Check_MK for the host where the script is installed.
- enjoy

# ToDo:
- more values: i.e. count of APs or radios online/up

