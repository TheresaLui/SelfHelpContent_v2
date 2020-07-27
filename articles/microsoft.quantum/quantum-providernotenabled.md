<properties
	pageTitle="A Provider or Target is not enabled in your Workspace"
	description="When you attempt to submit a job it fails because the provider or target is not enabled in your Workspace."
	infoBubbleText="Common Solutions Template"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="mblouin"
	displayOrder=""
	articleId="quantum-providernotenabled"
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# A Provider or Target is not enabled in your Workspace

When you attempt to submit a job you may receive either of the below errors:

- `The provider specified does not exist or is not enabled for the workspace`
- `The target specified does not exist or is not enabled for the workspace`

This error occurs when you have not enabled the requested provider in your workspace, or have not selected a Plan that gives you access to the desired target.

It is also possible that the desired target/provider combination does not exist.

## **Recommended Steps**

1. Navigate to your Quantum Workspace resource in the Portal
1. Select the `Providers` blade
	TODO: Can we link to the blade dynamically? (data-blade:extensionName.bladeName.nameOfInputParam.valueOfInputParam)
1. If you see the desired provider enabled in the list of providers, follow the instructions below under "Modify a Provider". Otherwise, follow the instructions under "Enable a Provider".

### Enable a Provider

If you have not already enabled the provider in your workspace, you will need to enable them. From the `Providers` blade of your Quantum Workspace:

1. Select the "Add a provider" button at the top of the blade
1. Find the desired provider in the list of providers and select "Add"
1. Identify the plan which gives you access to the desired Target. You may need to reference the providers' documentation.
1. Accept the providers terms, and click `Enable`
1. Wait for the deployment to complete and try submitting a job against the provider

### Modify a Provider

If you have enabled the provider, you may not have selected a plan which allows you to access your desired target. From the `Providers` blade of your Quantum Workspace:

1. Find the provider in the list of enabled providers
1. Select "Modify"
1. Identify the plan which gives you access to the desired Target. You may need to reference the providers' documentation.
1. Accept the providers terms, and click `Enable`
1. Wait for the deployment to complete and try submitting a job against the provider

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
