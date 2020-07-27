<properties
	pageTitle="Permission denied Creating, Reading, or Cancelling jobs"
	description="When you attempt to perform an operation on the jobs in a workspace but you receive a permission denied (403 Forbidden) error"
	infoBubbleText="Permission Denied Error"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="mblouin"
	displayOrder=""
	articleId="quantum-permissions-dataplane"
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# Performing an operation on the jobs in a workspace yields a 'Permission Denied' (403 Forbidden) error code

Azure Quantum uses RBAC (role based access contorl) to manage access rights for users and entities. You may receive an error if your workspace's permissions are not configured correctly. 

## **Recommended Steps**

1. If you are new to RBAC permissions, please start by reviewing the [general RBAC documenation](https://docs.microsoft.com/en-us/azure/role-based-access-control/)
2. Review the TODO: Can we link to the blade dynamically? [access control blade](data-blade:extensionName.bladeName.nameOfInputParam.valueOfInputParam) of your quantum workspace
3. Reference the Azure Quantum [documentation on RBAC roles]() and ensure that you have the required permissions to complete the operation that you are trying to carry out

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
