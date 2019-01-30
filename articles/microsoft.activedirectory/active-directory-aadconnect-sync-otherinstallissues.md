<properties
    articleid="36c550bc-6887-42ca-a367-9f8ac1f234c1"
    pageTitle="Azure AD Connect install issues"
    description="Azure AD Connect install issues"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629791"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public"
    />

# Azure AD Connect install issues

## **Recommended Steps**
Please check which [Azure AD Connect installation type](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation) is suitable for you. If you meet the criteria of express installation, then we highly recommend you to go with the express installation. The express installation gives you minimal options needed to finish the installation, therefore there is less likelihood of any issues. 

However, if you don�t meet the express installation criteria and must do the custom installation then here are some best practices you can follow to avoid common issues. For the sake of simplicity only selective options are mentioned here:

* Ensure you are an administrator on the machine on which you are installing AAD Connect. Log in on to the machine with same administrator credentials.

* Let all the options to be default on the following page, except for �Use an existing SQL Server�, if you want to use existing SQL Server. Here are [more details](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom) about how to use custom installation options. 

    ![Use Existing SQL Server](./media/aadconnect-sync-otherinstallissues/useexistingsqlserver.png)

* On the following page, pick option �Create new AD account", to avoid any permission issues with existing account.

    ![AD Forest Account](./media/aadconnect-sync-otherinstallissues/createnewaccount.png)

### **Common Issues**

* [Connectivity issues with on-premise Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools).

* [Connectivity issues with online Azure Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity).

* [Permission issues with on-premise Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account).

## **Recommended Documents**
* [Prerequisites for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites)
* [Select which installation type to use for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation)
* [Getting started with Azure AD Connect using express settings](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express)
* [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)
* [Azure AD Connect: Upgrade from a previous version to the latest](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-upgrade-previous-version)
* [Azure AD Connect: What is staging server?](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-topologies#staging-server)
* [What is the ADConnectivityTool PowerShell Module?](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)