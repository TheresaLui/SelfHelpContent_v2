<properties
    pageTitle="I have a problem with a single object not syncing (correctly)"
    description="I have a problem with a single object not syncing (correctly)"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32684507"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="8f7d2d3f-5f4e-41e8-86c6-70987bead134"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# I have a problem with a single object not syncing (correctly)

## **Recommended Steps**

For Azure AD Connect deployment with **version 1.1.749.0 or higher**, [use the troubleshooting task in the wizard](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync#run-the-troubleshooting-task-in-the-wizard) to troubleshoot object synchronization issues. This task will investigate your environment and will report any issues it can find. Note that you can also use the troubleshooting task in the wizard to sync a single object from AD to AAD - the troubleshooting task will report the outcome of all the steps, which is usually sufficient to pin point what the problem is with syncing a single object.

For **older versions**, [review how objects flow in AAD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing) and begin troubleshooting from there.

## **Recommended Documents**

* [Troubleshoot AAD Connect object not syncing](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)
* [Troubleshooting task in the wizard](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync#run-the-troubleshooting-task-in-the-wizard)
