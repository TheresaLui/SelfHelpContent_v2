<properties
	pageTitle="Backup best practices"
	description="Backup best practices"
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
	articleId="e8fcfbb2-d72c-4225-8fbb-be89443e87aa"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Backup best practices

<!--issueDescription-->

When you're configuring VM backups, we suggest following these practices:

1. Modify the default schedule times that are set in a policy. For example, if the default time in the policy is 12:00 AM, increment the timing by several minutes so that resources are optimally used.<br>
2. For backup of VMs that are using premium storage, with Instant Restore, we recommend allocating 50% free space of the total allocated storage space, which is required only for the first backup. The 50% free space is not a requirement for backups after the first backup is complete<br>
3. The limit on the number of disks per storage account is relative to how heavily the disks are being accessed by applications that are running on an infrastructure as a service (IaaS) VM. As a general practice, if 5 to 10 disks or more are present on a single storage account, balance the load by moving some disks to separate storage accounts.<br>

<!--/issueDescription-->

