<properties
    pageTitle="Problems with policy not being enforced"
    description="Problems with policy not being enforced"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="14fe722d-a90d-40f1-86d7-da02e95348ce"
	ownershipId="AzureIdentity_User"
/>

# Problems with policy not being enforced


**I encounter different results depending on the mobile or desktop application I use.**

Conditional access policy is supported in the browser and using applications with modern authentication. Older versions of Office, like Office 2010 or Office 2013 without modern authentication use different security protocols that need to be locked down at ADFS. This is done by authoring ADFS issuance authorization rules.
<br><br>
The following document explains how to lock down older protocols with ADFS:
<br>
[How to configure conditional access for Office 365 SharePoint and Exchange](https://docs.microsoft.com/azure/active-directory/conditional-access/block-legacy-authentication)


**I don't see conditional access policy being enforced for any applications**

Conditional access policy changes can take up to five minutes to take effect. If you just made the policy change, please wait for five minutes and try again. If that doesn't resolve the problem, you can review policy and make sure all conditions apply. For example, is policy applied to the user and application that is being tested.
<br><br>
For more details, see:
<br>
[How are conditions used to trigger policy controls](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)