# Automate-Azure-VM-Start-Stop-using-tags
This Power shell script can be used to start/stop your Azure Virtual Machines by adding the desired start/stop time in the VM's tags .


This particular script can be scheduled using Azure Automation , a service provided by Azure for scheduling jobs.

Consider you have a huge development / non-production workload running on Azure, it is best to stop your non-critical Virtual Machines during non-business hours. 

Since Azure charges Virtual Machines for every hour it is running, stopping these VMs during non-business hours can save huge money.

All you have to do is schedule the script in Azure Automation and add a tag to your VM like below with the deisred time

VMStartTimeinUTC : 09:00
ShutdownTimeinUTC : 20:00

