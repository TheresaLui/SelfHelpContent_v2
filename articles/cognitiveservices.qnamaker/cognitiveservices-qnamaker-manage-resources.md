<properties
	pageTitle="Manage QnA Maker Resources"
	description="Manage QnA Maker Resources"
	service="cognitiveService-qnamaker"
	resource="qnamaker"
	authors="nerajput1607"
	ms.author="nerajput"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32689779,32689762,32689800,32689786,32689784"
	resourceTags=""
	productPesIds="16919"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="b97a4b1c-4d63-468b-4ded-fcda14edd5fe"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Manage QnA Maker Resources

### **Frequently asked questions**

* **Why is my service region shown as West-US, when I selected some other region?**<br>
Your data is stored in the region you choose for your Azure Search Service and App Service. [QnA Maker management layer is present in only West-US](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#management-service-region) which is used for only QnA Maker portal and no customer data is stored there ever. 

* **What are the recommended settings for my target QPS?**<br>
You need to select the tiers for App Service and Azure Cognitive Service based on your expected QPS, please check the [Recommended Settings](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#recommended-settings).

* **When should I change my pricing tier?**<br>
You may need to change your pricing tier for any of the three services or all of them. It only depends on your scenario, whether you are expecting more traffic or you want to support more number of Knowledge bases or you want to have more QnA pairs. For more details, see [When to change a pricing tier](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#when-to-change-a-pricing-tier).


## **Recommended Documents**

* [Resource planning and pricing tier consideration](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources)
* [Manage QnA Maker Resources](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure)
* [Disaster Recovery and Backup using traffic manager](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure#business-continuity-with-traffic-manager)
