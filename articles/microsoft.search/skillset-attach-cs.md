<properties
	pageTitle="Issue attaching cognitive services resource"
	description="Only a small number of documents get processed through skillset"
	service="microsoft.search"
	resource="searchservices"
	authors="luiscabrer"
	ms.author="luisca"
	selfHelpType="resource"
	displayOrder="1"
	supportTopicIds="32681353"
	resourceTags=""
	productPesIds="15568"
	articleId="skillset-attach-cs"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue attaching cognitive services resource

## **Recommended Steps**

If you don't attach a cognitive services resource to your skillset, you may get an error that says that the indexing stopped because the *"free skillset execution quota exceeded"*. This means that you have exceeded the number of documents you can enrich for free  (20 documents per day). If that is the case you can attach a billable Cognitive Services resource to a skillset for larger and more frequent workloads. 

[This article](https://docs.microsoft.com/azure/search/cognitive-search-attach-cognitive-services) describes how to attach a cognitive services resource to your skillset.

It is important to note that your Cognitive Services resource must be in the **same region** as your Azure Service.

If you want to attach a cognitive service resource programmatically, please see [this section of the documentation](https://docs.microsoft.com/azure/search/cognitive-search-attach-cognitive-services).

## **Recommended Documents**

* [Attach a cognitive services resource to a skillset](https://docs.microsoft.com/azure/search/cognitive-search-attach-cognitive-services) <br
