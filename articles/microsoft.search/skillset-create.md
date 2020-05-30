<properties
	pageTitle="Issue creating or editing a skillset"
	description="Issue creating or editing a skillset"
	service="microsoft.search"
	resource="searchservices"
	authors="luiscabrer"
	ms.author="luisca"
	selfHelpType="resource"
	displayOrder="6"
	supportTopicIds="32681358"
	resourceTags=""
	productPesIds="15568"
    articleId="skillset-create"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating or editing a skillset

## **Recommended Steps**

These are some issues you may encounter with your skillset:

1. If you are new to creating a skillset, you may want to learn how to do it using the [portal](https://docs.microsoft.com/azure/search/cognitive-search-quickstart-blob), or learn [how to do it programmatically](https://docs.microsoft.com/azure/search/cognitive-search-defining-skillset). It is important to note that your Cognitive Services resource must be in the **same region** as your Azure Service.
1. If you get an error saying that there was a problem with a skill # *X*, and you are not sure what skill the error is referring to, a good practice is to set the name of each skill. You do that by setting the *name* property on the skill to a unique value. This will make the errors refer to the skill by name.
1. Always check that your skill inputs are correct. Remember that inputs are *case sensitive*. Also be careful not to add a "slash" at the end of an input path by mistake. For instance "/document/normalized_images" is not the same as "/document/normalized_images/". The latter refers to a value with an empty name that is a child of the normalizes_images element, and not to the normalized_images element itself.
1. When running your indexer, you may get an error that says that the indexing stopped because the *"free skillset execution quota exceeded"*. This means that you have exceeded the number of documents you can enrich for free. If that is the case you can attach a billable Cognitive Services resource to a skillset for larger and more frequent workloads. [This article](https://docs.microsoft.com/azure/search/cognitive-search-attach-cognitive-services) describes how to attach a cognitive services resource to your skillset.
	
## **Recommended Documents**

* [How to create a skillset in an enrichment pipeline](https://docs.microsoft.com/azure/search/cognitive-search-defining-skillset)
* [Create Skillset REST API Reference page](https://docs.microsoft.com/rest/api/searchservice/create-skillset)
* [How to reference annotations in a cognitive search skillset](https://docs.microsoft.com/azure/search/cognitive-search-concept-annotations-syntax)
* [How to add a custom skill to a cognitive search pipeline](https://docs.microsoft.com/azure/search/cognitive-search-custom-skill-interface) 
* [Quickstart: Create an AI indexing pipeline using cognitive skills on the Azure Portal](https://docs.microsoft.com/azure/search/cognitive-search-quickstart-blob)
