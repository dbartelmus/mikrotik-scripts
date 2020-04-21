# mikrotik-scripts
scripting Mikrotik's RouterOS, SwitchOS, routers, switches, devices

# what's up?
This is decent MikroTik OS configuration backup to e-amil script.

Once executed:
- it creates device configuration backup file
- then sends email
- then delete backup
- then log (save) action in router logs

# how to install
1. you need to configure SMTP to properly send emails - "Tools" -> "email"
2. you need to copy/paste script to your router "System -> "Scripts" 
* name it as follow: backup-to-email
* change this line with your email:  /tool e-mail send file="$filename" to="your-email@domain.com" subject="$subject";
* at this time feel free to hit "Run Script" button
3. create "System" -> "Scheduler" event with following "On event" field:
* /system script run backup-to-email


# enjoy, feel free to update/modify
