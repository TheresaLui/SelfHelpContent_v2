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
Your data is stored in the region you choose for your Azure Search Service and App Service. [QnA Maker management layer is only present in West-US](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources#management-service-region) and is used for only the QnA Maker portal. No customer data is stored there ever.

* **Why am I unable to create a QnA Maker Service?**<br>
We allow only one free QnA Maker service per subscription. Either upgrade to the standard tier, or delete the existing one and create another. 

* **How do I add a language-specific KB to my existing service?**<br>
In the current GA model, language setting is specific to each Service. You cannot have KBs belonging to different languages in a single service. You can create a new service in public preview, which gives you an option to specify languages for KBs.
 This setting is only enabled the first time you create the KB. For details, review [language settings for QnA Maker](https://docs.microsoft.com/azure/cognitive-services/qnamaker/overview/language-support?tabs=v2).

* **How do I use an existing app service plan?**<br>
While creating a QnA Maker resource in the current GA model, a new app service plan is created for the user. The user is allowed to change it to the existing app service plan. [See documentation for more details](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure?tabs=v1#upgrade-app-service).

* **How do I change/update my Azure Search SKU?**<br>
There is no automated way to update the Azure Search SKU. Here are the [steps to upgrade your Azure Search Service](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure?tabs=v1#upgrade-the-azure-cognitive-search-service)

* **Why am I getting a Bad Arguments error during KB creation?**<br>
It can be due to extraction failure, please check out the [document types we support.](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/data-sources-and-content) and data [format guidelines.](https://docs.microsoft.com/azure/cognitive-services/qnamaker/reference-document-format-guidelines)

* **Why am I getting no endpoint key found error?**<br>
There can be several reasons why you are seeing this error. 
	* Check if the firewall is preventing the communication with App Service. [Please read about network isolation in App Service](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure?tabs=v1#network-isolation-for-app-service).
	* If you are using an ARM template to create the QnA Maker resource, the ARM template may be missing some configuration. Add the below fields in the ARM template as part of the App Service creation:
`"PrimaryEndpointKey": "[concat(parameters('appName'), '-PrimaryEndpointKey')]", 
"SecondaryEndpointKey": "[concat(parameters('appName'), '-SecondaryEndpointKey')]",`

   To reference the ARM template that is generated when creating a QnA Maker resource in the portal, select **Automation options** on the Review + create screen.

## **Recommended Documents**

* [Resource planning and pricing tier consideration](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/azure-resources)
* [Manage QnA Maker Resources](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure)
