<properties
	pageTitle="Issues with running skillsets at scale"
	description="Issues with running skillsets at scale"
	service="microsoft.search"
	resource="searchservices"
	authors="MarkHeff"
	ms.author="maheff"
	selfHelpType="resource"
	supportTopicIds="32681379"
	displayOrder="35"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="skillset-running-at-scale"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issues with running skillsets at scale

## **Recommended Steps**

If you are having trouble running a skillset at scale:

1. Make sure to [add a Cognitive Services resource to the skillset](https://docs.microsoft.com/azure/search/cognitive-search-attach-cognitive-services). A limited number of documents will be enriched for free but for larger and more frequent workloads, you should attach a billable Cognitive Services resource.
1. Confirm that the names and sources of the inputs to your skills are valid. It can be useful to draw out the structure of your annotations to confirm that the input to a skill is correct. More information about how to reference annotations in a skillset can be found [here](https://docs.microsoft.com/azure/search/cognitive-search-concept-annotations-syntax).
1. Confirm that the name and target name for the outputs to your skills are valid.
1. Check that the right context has been set for every skill in the skillset. More information about the context can be found [here](https://docs.microsoft.com/azure/search/cognitive-search-defining-skillset#add-built-in-skills).

## **Recommended Documents**

* [Creating a skillset](https://docs.microsoft.com/azure/search/cognitive-search-defining-skillset)
* [How to reference annotations in a skillset](https://docs.microsoft.com/azure/search/cognitive-search-concept-annotations-syntax)