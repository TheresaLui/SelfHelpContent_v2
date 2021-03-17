<properties
	pageTitle="App Service"
	description="App service"
	service="cognitiveService-qnamaker"
	resource="qnamaker"
	authors="DishaAgarwal"
	ms.author="diagarw"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32689756"
	resourceTags=""
	productPesIds="16919"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="1ed2aae3-0368-0b9b-054a-8d42b5881fae"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# QnA components

### **Frequently asked questions**

* **Can we share the QnA Maker App Service with other services?**<br>
You shouldn't share the same QnA Maker App Service. But you can share the 'App Service Plan'. Please find the details [here](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#share-services-with-qna-maker).

* **How to configure App Service to handle more RPS (Request Per Second)?**<br>
You have full control to scale up/down the app service as per your RPS needs. You can find the recommended settings [here](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#recommended-settings).

* **Why is my service region shown as West-US, when I selected some other region?**<br>
Your data is stored in the region you choose for your Azure Search Service and App Service. [QnA Maker management layer is present in only West-US](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#management-service-region) which is used for only QnA Maker portal and no customer data is stored there ever.

## **Recommended Documents**

* [Manage and Customize QnA Maker Azure Resources](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources)
