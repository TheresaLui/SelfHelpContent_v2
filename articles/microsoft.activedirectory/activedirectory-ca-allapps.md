<properties
    pageTitle="Problems setting policy that applies to 'all cloud apps'"
    description="Problems setting policy that applies to 'all cloud apps'"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="abea3942-6908-4302-8148-ce816f6e2e57"
	ownershipId="AzureIdentity_User"
/>

# Problems setting policy that applies to 'all cloud apps'

Conditional access policy that applies to 'all cloud apps' will be enforced for any web site or web service. This includes the Azure Portal. Because the policy has a broad impact it is recommended that policy gets rolled out and verified with a small set of users before it is rolled out to all users.

## **Recommended steps**

*	When policy is applied to all clouds, make sure administrator accounts are excluded
*	Ensure policy behaves as expected before applying to administrator accounts

For more details, see:
<br>
[How to avoid account lock out when setting conditional access](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal#what-you-should-avoid-doing)