<properties
	pageTitle="Why aren't access packages showing up in a user's MyAccess portal?"
	description="Access package not showing up in a user's MyAccess portal."
	service="microsoft.aad"
	resource="Microsoft_AAD_ERM"
	authors="kyschaub"
	ms.author="kyschaub"
	displayOrder="32"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="governance_overview"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="activedirectory-iga-missing-packages-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Why aren't access packages showing up in a user's MyAccess portal?

## **Recommended Steps**

1. In the Azure portal, open the access package and then click **Policies**
2. Ensure that you have a policy that includes the user. The user should be selected or be in a selected group or directory.
3. In the **Policy details** pane for this policy, ensure the **Enabled** property is set to **Yes**
4. Click **Overview** for the access package and ensure the **Hidden** property is set to **No**
5. Open the catalog the access package is in, click **Overview**, and ensure the **Enabled** property is set to **Yes**
6. If the user is an external user, ensure the **Externally visible** property for the catalog is set to **Yes**
