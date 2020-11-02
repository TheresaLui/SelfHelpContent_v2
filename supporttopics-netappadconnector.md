<properties
	pageTitle="Unable to add backup operator"
	description="Unable to add backup operator"
	service="microsoft.storage"
	resource="storage"
	authors="b-avaish"
	ms.author="b-avaish"
	displayOrder=""
	articleId="NetAppbackupoperator"
	selfHelpType="generic"
	supportTopicIds="32777926"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# NetApp Volumes Active Directory Domain Services and Authentication

## **Recommended Steps**

1.Make sure you are whitelisted for the Backupoperator Afec. Below is az cli command:
Get-AzProviderFeature -ProviderNamespace Microsoft.Netapp -FeatureName ANFBackupOperator
2.If not registered, please register with below command:
Register-AzProviderFeature-ProviderNamespace Microsoft.NetApp -FeatureName ANFBackupOperator
## **Recommended Documents**

-(https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)<br>