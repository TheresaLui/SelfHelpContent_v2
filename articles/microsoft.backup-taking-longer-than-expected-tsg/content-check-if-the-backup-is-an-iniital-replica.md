<properties
	pageTitle="Check if the backup is an initial replica"
	description="Check if the backup is an initial replica"
	service=""
	resource=""
	authors="TestAuthor"
	ms.author="TestAuthor"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d59bca2a-c7d5-4709-b687-09353f0cec78"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if the backup is an initial replica

1. Confirm with the customer if this the initial backup of the VM or if they have added or moved any disk of the VM since last backups
2. You can also double check our telemetry using the TaskId collected on the previous step.

**Important:** 
	1. Make sure you are on the right MAB cluster when runnign the query 
	2. Note only completed job will be seen. If the job is still running make sure to check information with customer
	
~~~kusto

BCMBackupStats
| where TaskId == <TaskId> // Replace <TaskId> with the guid collected on step 1
| project IsIR, VMName, TaskId

~~~

If isIR column result is 1 this job was an initial replica for the whole VM

You can also check if the number of disk did change on the job. 

~~~kusto

 BCMBackupStats
| where TaskId == <TaskId> // Replace <TaskId> with the guid collected on step 1
| project NumberOfDisks, NumberOfDiskAdded, VMName, TaskId

~~~

If NumberOfDiskAdded is greather than 0, then this job has an initial replica of a disk
