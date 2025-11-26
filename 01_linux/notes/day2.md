## Permission Error Lab

### Scenario 1 — Log file unwritable
Error: Permission denied when app tried to write to app/logs/app.log  
Cause: chmod 400 removed write permission  
Fix: chmod 640 app/logs/app.log  

https://github.com/takiahoward/cloud-engineering-journey/blob/49f2a7cf3f7f3c965a2ce7b26bea0ddd47beaee3/01_linux/images/permission_lab_1.png

### Scenario 2 — Config owned by root
Error: Cannot save changes to app/config/config.yaml  
Cause: Owned by root:root  
Fix: sudo chown $USER:$USER app/config/config.yaml  

https://github.com/takiahoward/cloud-engineering-journey/blob/49f2a7cf3f7f3c965a2ce7b26bea0ddd47beaee3/01_linux/images/permission_lab_2a.png

https://github.com/takiahoward/cloud-engineering-journey/blob/49f2a7cf3f7f3c965a2ce7b26bea0ddd47beaee3/01_linux/images/permission_lab_2b.png


### Scenario 3 — Script not executable
Error: Permission denied running ./app/scripts/start.sh  
Cause: chmod 644 removed execute bit  
Fix: chmod +x app/scripts/start.sh  

https://github.com/takiahoward/cloud-engineering-journey/blob/49f2a7cf3f7f3c965a2ce7b26bea0ddd47beaee3/01_linux/images/permission_lab_3.png

### Scenario 4 — Logs directory not accessible
Error: Permission denied listing app/logs  
Cause: Directory missing execute permission  
Fix: chmod 750 app/logs


https://github.com/takiahoward/cloud-engineering-journey/blob/49f2a7cf3f7f3c965a2ce7b26bea0ddd47beaee3/01_linux/images/permission_lab_4.png


