<properties
	pageTitle="Issue creating knowledge store projections"
	description="Issue creating knowledge store projections"
	service="microsoft.search"
	resource="searchservices"
	authors="vkurpad"
	ms.author="vikurpad"
	selfHelpType="resource"
	displayOrder="4"	
	supportTopicIds="32681339"
	resourceTags=""
	productPesIds="15568"
	articleId="knowledge-store-projection"
	cloudEnvironments="public"
/>
# Issue creating a knowledge store projection

## **Recommended Steps**

If you are having trouble with creating a knowledge store projection you may want to ensure that:

1. Define the knowledge store with a connection string and projections in the skillset as described [here](https://docs.microsoft.com/en-us/azure/search/knowledge-store-projection-overview)
1. Use a shaper field to create a shape to match the projection definition
1. Ensure that the names and case of the projection names match the enrichment
	
## **Recommended Documents**

* [Working with projections in a knowledge store in Azure Search](https://docs.microsoft.com/en-us/azure/search/knowledge-store-projection-overview) 
