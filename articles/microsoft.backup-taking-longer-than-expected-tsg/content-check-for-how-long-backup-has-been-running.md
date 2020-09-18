<properties
	pageTitle="Check for how long the backup has being running "
	description="Check for how long the backup has being running "
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
	articleId="969821cd-420e-4522-9960-4ca0d8cae448"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check for how long the backup has being running 

1. Navigate to BackupsJobs tab on ASC for the Vault
2. Select backup Management type : IAAS VM  and complete the container name with the Name of VM 
3. Confirm the job completed that took longer than expected reviewing "Duration (in sec)"
4. Take note of the TaskId  for future refence and troubleshooting

If job that is taking longer has not yet completed, please collect the current running job information with customer from  portal -> Vault -->Backup jobs-> and "Export jobs". Take note of the Activity ID on the excel file for the relevant job ( it will be called TaskId on our internal queries) 
