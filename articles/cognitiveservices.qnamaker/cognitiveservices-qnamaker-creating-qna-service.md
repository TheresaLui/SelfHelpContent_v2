<properties
  pagetitle="Creating a QnA Service&#xD;"
  service="cognitiveservice-qnamaker"
  resource="qnamaker"
  ms.author="diagarw,nerajput"
  selfhelptype="Generic"
  supporttopicids="32689804,32689805"
  resourcetags=""
  productpesids="16919"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="1b0b30f9-3934-746d-c74f-c0216466891f"
  ownershipid="AzureCogSvc_CognitiveServices" />
# Creating a QnA Service

### **Frequently asked questions**

* **Why is my service region shown as West-US, when I selected some other region?**<br>
Your data is stored in the region you choose for your Azure Search Service and App Service. [QnA Maker management layer is present in only West-US](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#management-service-region) which is used for only QnA Maker portal and no customer data is stored there ever.

* **Why am I unable to create a QnA Maker Service?**
We allow only one free QnA Maker service per subscription, either upgrade to the standard tier or delete the existing one and create another. 

* **How do I add language specific KB to my existing service?**
In current GA model, language setting is specific to one Service, you cannot have KBs belonging to different language in one service. You can create a new service in public preview, which gives you an option to make language setting KB specific.
 This setting is enabled only for the first time you are creating the KB. Please check [language settings for QnA Maker managed for more details.](https://docs.microsoft.com/azure/cognitive-services/qnamaker/overview/language-support?tabs=v2)  

* **How to use an existing app service plan?**
While creating a QnA Maker resource in current GA model, we create a new app service plan for the user. The user is allowed to change it to the existing app service plan. [Please check documentation for more details.](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure?tabs=v1#upgrade-app-service) 

* **How to change/update my Azure Search SKU?**
There is no automated way to update the Azure Search SKU. Here are the [steps to upgrade your Azure Search Service](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure?tabs=v1#upgrade-the-azure-cognitive-search-service)

* **Why am I getting Bad Arguments error during KB creation?**
It can be due to extraction failure, please check out the [document types we support.](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/data-sources-and-content) and data [format guidelines.](https://docs.microsoft.com/azure/cognitive-services/qnamaker/reference-document-format-guidelines)

* **Why am I getting no endpoint key found error ?**
There can be several reasons why you are seeing this error. 
	* Please check if the firewall is preventing the communication with App Service. [Please read about network isolation in App Service](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure?tabs=v1#network-isolation-for-app-service).
	* If you are using an ARM template to create QnA Maker resource then you might be missing some configuration in the ARM template. Add the below fields in the ARM template as part of the App Service creation:
"PrimaryEndpointKey": "[concat(parameters('appName'), '-PrimaryEndpointKey')]", 
"SecondaryEndpointKey": "[concat(parameters('appName'), '-SecondaryEndpointKey')]", 
You can reference the ARM template that is generated when creating a QnA Maker resource in portal and selecting "Automation options" at the Review + create screen.
## **Recommended Documents**

* [Resource planning and pricing tier consideration](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources)
* [Manage QnA Maker Resources](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure)