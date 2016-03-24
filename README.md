
#Shell Script to Restart the Services if Down/Crashed

autostart-nginx-php-mysql

It’s common for process to crash/go down due to various reasons, which you can investigate and fix the issues but that may take little time. However, one thing you can do it immediately to reduce the downtime for better availability is to automate restart of the process if it’s down.

Let’s get this done through the free way – shell scripts

You can use following shell scripts to run through crontab, which will check the services at every 5 minutes (you can adjust the interval time) and will start if found not running. Sounds cool?



#Create your script and add it to the /opt/ folder.

1. run -  "update-rc.d cron defaults"
2. run - "/etc/init.d/cron start"
3. run - "nano /opt/startifdown.sh" 
4. copy the bash code to your script 
5. run "crontab -e"
6. Add the code at bottom (note this cron is for 5m in 5m) .   */5 * * * * /opt/startifdown.sh >/dev/null 2>&1  
7. Be sure the scrip is executable: run - "chmod +x /opt/startifdown.sh" 

