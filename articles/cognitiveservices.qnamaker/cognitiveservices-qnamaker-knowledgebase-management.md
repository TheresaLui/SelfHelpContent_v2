
<properties
	pageTitle="Knowledge Base Management"
	description="Knowledge Base Management"
	service="cognitiveService-qnamaker"
	resource="qnamaker"
	authors="nerajput1607"
	ms.author="nerajput"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32689761,32689760,32689776,32689785"
	resourceTags=""
	productPesIds="16919"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="2fb8a8bf-87a6-550c-48d0-f300535d5d3e"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# Knowledge Base Management

### **Frequently asked questions**

* **How can I set a language for my Knowledge Base?**<br>
Language setting is specific to every service. QnA Maker allows you to select the language for your QnA service, while creating the first knowledge base. For all the knowledge bases in a QnA Maker resource, they all must be in the same language. This language can't be changed. Please check [language concepts applicable in QnA Maker](https://docs.microsoft.com/azure/cognitive-services/QnAMaker/how-to/language-knowledge-base#verify-language). 

* **Is there a  way to recover a Knowledge base that has been deleted by mistake?**<br>
Based on Data Protection Policy, QnA Maker does not keep any user data. User has to create a new QnA Maker again and load all QnA pairs to the knowledge base. 

* **What is the process of importing a Knowledge Base?**<br>
Importing a Knowledge base replaces the existing content in the Knowledge base, it requires the content to be in .tsv structured format, you can also import multi-turn based Knowledge base. Please check [structured data format through import](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/knowledge-base#structured-data-format-through-import) for more details.

* **What are the content types supported and what is the exact format of data to be used?**<br>
Data sources location should be public urls and files that don't require any authentication. Please check [Content type supported for creating a knowledge base](https://docs.microsoft.com/azure/cognitive-services/qnamaker/concepts/content-types) to know the formats for the files. <br>
SharePoint files with authentication are also supported but resources must be files, not web pages. If the URL ends with a web extension, such as .ASPX, it will not import into QnA Maker from SharePoint. Please check the [prerequisites and steps to add SharePoint files as data source in your knowledge base](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/add-sharepoint-datasources).

* **How to add Chit-chat datasets to my knowledge base?**
Chit-chat data sets are used to add personality to your Knowledge Base. These data sets makes the bots more conversational and engaging, these are available in 5 different personas. Please check the [steps to add personality to your Knowledge Base](https://docs.microsoft.com/azure/cognitive-services/qnamaker/how-to/chit-chat-knowledge-base).

## **Recommended Documents**

* [Troubleshooting FAQs for managing a knowledge base](https://docs.microsoft.com/azure/cognitive-services/QnAMaker/troubleshooting#manage-the-knowledge-base)
* [Steps to create and manage a knowledge base](https://docs.microsoft.com/azure/cognitive-services/qnamaker/quickstarts/create-publish-knowledge-base)
* [Create Knowledge Base and manage settings](https://docs.microsoft.com/azure/cognitive-services/QnAMaker/how-to/manage-knowledge-bases)
