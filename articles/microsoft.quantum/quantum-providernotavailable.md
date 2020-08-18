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

Not every provider is available in every Azure region where Azure Quantum is available.

The *recommended steps* below should help you work out if a provider should be available in your region.

## **Recommended Steps**

1. Please review our [provider documentation](https://github.com/MicrosoftDocs/quantum-docs-private/wiki/Azure-Quantum-provider) to check if your desired provider is available in your region.
   * If trying to add a third-party provider consider contacting them directly for more details regarding availability in the region you would like to use
2. If using the CLI, verify that the provider/target combination that you are requesting is valid.
3. If unsure, deploy a workspace in a different region to check if the provider is available to select there.

## **Recommended Documents**

*Please note that our documentation for Azure Quantum is in limited preview. Only customers currently in the limited preview can access the documentation resources linked.*
* [Azure Quantum QIO Provider](https://github.com/MicrosoftDocs/quantum-docs-private/wiki/Azure-Quantum-provider)
* [IonQ Provider](https://github.com/MicrosoftDocs/quantum-docs-private/wiki/IonQ-provider)