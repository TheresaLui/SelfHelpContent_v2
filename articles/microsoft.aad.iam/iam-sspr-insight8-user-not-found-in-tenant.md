<properties
    pageTitle="User is not found in your tenant"
    description="User is not found in your tenant"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    ms.author="srsridh"
    authors="srinathsridhar"
    displayOrder="1"
    articleId="User_Not_Found_In_Tenant"
    selfHelpType="diagnostics"
    diagnosticScenario="health_diagnostic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Blackforest, Mooncake, usnat, ussec"
	  ownershipId="AzureIdentity_B2B"
/>

# User is not found in your tenant
<!--issueDescription-->
User <!--$UserId-->[UserId]<!--/$UserId--> is not found in your Azure AD tenant.
<!--/issueDescription-->

## **Recommended Steps**

* Try searching for the user using their user principal name
* If searching using the user principal name yielded no results, then try searching using the user's object id instead
* If searching using the user principal name or the object id yielded no results, then this user is not a member of your Azure AD tenant
