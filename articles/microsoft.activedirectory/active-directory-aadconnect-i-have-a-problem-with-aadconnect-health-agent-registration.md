<properties
    pageTitle="I have a problem with AADConnect Health Agent registration"
    description="I have a problem with AADConnect Health Agent registration"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32689666"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="1a1f6796-7eb0-4dbe-a202-41b66e9bd6e2"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# I have a problem with AADConnect Health Agent registration
## **Recommended Steps**
1.	Ensure you are authorized to perform the operation. Global Admins have access by default. Additionally, you can use [Role Based Access Control](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-operations#manage-access-with-role-based-access-control) to delegate registration permission to Contributor.
2.	Ensure the required endpoints are enabled, and not blocked due to firewall. See [requirements](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-agent-install) section for details. 
3.	Registration can fail due to outbound communication being subjected to SSL inspection by the network layer

## **Recommended Documents**

* [Common installation questions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-health-faq)
