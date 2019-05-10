<properties
	pageTitle="Why did snapshot fail?"
	description="Why did snapshot fail?"
	service="Microsoft.DataShare"
	resource="accounts"
	authors="mkadiri3"
	authoralias="makadiri"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="1d423bf5-f0a3-48fc-a6a1-314e04ea791f"
/>

# Why did snapshot fail?

Azure Data Share service needs permission to the Storage Account on the recipient side in order to write data into it. After the storage account is specified by the recipient, it could take a few minutes for the permission to take effect. If snapshot is triggered prior to it, it will fail. If you encounter failure, wait 5-10 minutes and try again.