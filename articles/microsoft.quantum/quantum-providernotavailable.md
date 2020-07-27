<properties
	pageTitle="A Provider is not available in your region"
	description="When you attempt to add a provider through the CLI you receive an error stating that the provider is not available in your region. It is also not available in the provider selection UI."
	infoBubbleText="Provider not available in a particular region"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="dasto"
	displayOrder=""
	articleId="quantum-providernotavailable"
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# A Provider is not available in a particular region

Not every provider is available in every Azure region where Azure Quantum is available. The *recommended steps* below should help you work out if a provider should be available in your region. 

## **Recommended Steps**

1. Please review our [provider documentation](https://) to check if your desired provider is available in your region.
   * If trying to add a third-party provider consider contacting them directly for more details regarding availability in the region you would like to use
2. If using the CLI, verify that the provider/target combination that you are requesting is valid.
3. If unsure, deploy a workspace in a different region to check if the provider is available to select there. 

## **Recommended Documents**

TODO: Add Documentation Links
* [This is the display text of an external document](https://)

### Notes

* The **Recommended Steps** and **Recommended Documents** headings must be entered as shown above (bolded H2)
* Formatting is not identical to Microsoft Docs - tables do not work, nor [!NOTE] tags
* Your Recommended Steps should be actual steps, not just links to other articles
* Ensure all links to Microsoft docs are non-region-specific, i.e. does not include /en-us/. This does not apply to articles for Mooncake.
* Don't link to internal review documentation - these URLs always start with "review.microsoft.docs", and users are unable to access them
* Do not use aka.ms links
* Copy the raw form of this article to use as a template for your own Common Solution article. Be sure to fill in the metadata!
