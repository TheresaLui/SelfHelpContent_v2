<properties
	pageTitle="Check if backups were taking less time before "
	description="Check if backups were taking less time before "
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
	articleId="9750d8e8-79f9-4412-bfa2-bec4930cae66"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if backups were taking less time before 

1. Go to ASC-> Resource Explorer -> Select the vault 
2. On the "Backup Jobs" tab. Select "Backup managment type" as IAAS VM and on container name complete the name of the VM. On Date Time select last 30 days
3. Select last jobs and review "Duration (in secs)" 
4. Confirm if previous backups were taking less time and change is significative enough.
