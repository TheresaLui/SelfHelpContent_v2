<properties
    pageTitle="Problems configuring policy for an application"
    description="Problems configuring policy for an application"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jcardena"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="conditionalaccess_overview"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="b06293cb-0562-4fac-84f4-55499112f001"
	ownershipId="AzureIdentity_User"
/>

# Problems configuring policy for an application

**I don't know which applications support conditional access**

Not all applications support conditional access. Supporting conditional access requires modern authentication and integration that allows device identities to be verified. We are continuing to increase the number of applications that are supported. The current list of applications can be found in the following documents.
<br>
[Which cloud applications support conditional access](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-technical-reference)<br>
[Which desktop and mobile applications support conditional access](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-supported-apps)

**I don't know how to secure older desktop applications?**

Conditional access policy is supported in the browser and using applications with modern authentication. Older versions of Office, like Office 2010 or Office 2013 without modern authentication use different security protocols that need to be locked down at ADFS. This is done by authoring ADFS issuance authorization rules.
<br><br>
The following document explains how to lock down older protocols with ADFS:
<br>
[How to configure conditional access for Office 365 SharePoint and Exchange](http://aka.ms/csforexchange)