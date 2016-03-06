
#Shell Script to Restart the Services if Down/Crashed

autostart-nginx-php-mysql

It’s common for process to crash/go down due to various reasons, which you can investigate and fix the issues but that may take little time. However, one thing you can do it immediately to reduce the downtime for better availability is to automate restart of the process if it’s down.

Let’s get this done through the free way – shell scripts

You can use following shell scripts to run through crontab, which will check the services at every 5 minutes (you can adjust the interval time) and will start if found not running. Sounds cool?
