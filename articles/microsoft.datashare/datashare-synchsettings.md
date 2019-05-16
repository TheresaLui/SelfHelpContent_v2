<properties
	pageTitle="Why is my synchronization setting not saved for my Data Share"
	description="Why is my synchronization setting not saved for my Data Share?"
	service="Microsoft.DataShare"
	resource="accounts"
	ms.author="joanpo"
	authors="joannapea"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="b8e6ed39-d79d-41f7-b2b3-02455066e8e1"
/>

# Why is my synchronization setting not saved for my Data Share?

When creating a Data Share, if the Data Provider does not enable a synchronization schedule for the Data Consumer to subscribe to, the Data Consumers data will not be automatically refreshed. Follow the below steps to resolve this issue:

## **Recommended Steps**

* Navigate to Azure Data Share -> Sent Shares and select the share in question
* Enable the ‘Scheduled refresh’ by using the slider and then use the drop down selector to specify a refresh interval
* Click ‘Save’ to save your changes
