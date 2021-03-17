
<properties
	pageTitle="Data Box setup and configuration"
	description="Learn how to resolve Network configuration issues for Data Box"
	service="microsoft.databox.jobs"
	resource=""
	authors="sunilrsanjeev"
	ms.author="sunir"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639191"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="32639191"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Azure Data Box setup and configuration

**Can't configure network for my Data Box**

Check if you are unable to connect to the Data Box because of any domain or group policy settings. If connecting via SMB, change the authentication level to 'NTLMv2 response only/refuse LM and NTLM' on the host.

## **Recommended Documents**
* [Data Box network configuration](https://docs.microsoft.com/azure/databox/data-box-deploy-set-up#connect-to-your-device)
* [Data Box cabling options](https://docs.microsoft.com/azure/databox/data-box-faq#configure-and-connect)
