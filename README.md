# Automate-Azure-VM-Start-Stop-using-tags
This Power shell script can be used to start/stop your Azure Virtual Machines by adding the desired start/stop time in the VM's tags .

Consider you have a huge development / non-production workload running on Azure, it is always best to stop your non-critical Virtual Machines during non-business hours. 

Since Azure charges Virtual Machines for every hour it is running, stopping these VMs during non-business hours can save huge money.

Yes, there is an option named Auto shut-down made available recently by Azure. But the major disadvantage of it is that you can't schedule your shut down time with this feature. You can only set the next shut down time. 

Also there are other traditional methods like using cron jobs for scheduled shutdown of servers. But Azure suggests to stop the VMs through Azure APIs or directly from the portal. Shutting down the VM directly from the server will put the VM in deallocated state for which Azure still continues to charge you.

So the best way is to automate the start/stop of your VMs using Azure Powershell. The PS script can be scheduled to run periodically using Azure Automation Service. There is a free usage of 500 minutes of Azure Automation Service every month which would suffice this. So actually you are paying nothing for scheduling your automation script.

All you have to do is schedule the script in Azure Automation and add a tag to your VM like below with the desired time

VMStartTimeinUTC : 09:00

ShutdownTimeinUTC : 20:00

