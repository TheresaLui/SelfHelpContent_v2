<properties
	pageTitle="UserErrorOperatingSystemFault"
	description="UserErrorOperatingSystemFault"
	infoBubbleText="SQL VDI initialization has failed."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererroroperatingsystemfault"
	diagnosticScenario="azurebackup-crc-usererroroperatingsystemfault"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorOperatingSystemFault

<!--issueDescription-->
We have identified that your operation failed because the paging file is too small.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue, verify the page file size settings to see if it is currently set to automatic. If it is then refer to this [guidelines](https://support.microsoft.com/help/2860880/how-to-determine-the-appropriate-page-file-size-for-64-bit-versions-of) and assign a custom size to the system drive.
