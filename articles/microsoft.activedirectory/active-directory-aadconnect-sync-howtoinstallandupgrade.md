<properties
    pageTitle="Azure AD Connect install and upgrade"
    description="Azure AD Connect install and upgrade"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629780"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="8ff8d9f2-9094-47f2-b305-a53350eb2d1f"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Azure AD Connect install and upgrade

## **Recommended Steps**

Best practices for installing and upgrading Azure AD Connect are found below. 

### **Clean Install**

* [Download the latest version of **Azure AD Connect**](https://www.microsoft.com/download/details.aspx?id=47594) and launch AzureADConnect.msi on the server where you want to install it. It is advised to install **Azure AD Connect** on a dedicated server.
* Please ensure you are logged in as Administrator on the server you are installing **Azure AD Connect**
* Select **Express** installation with default options if you meet following requirements:
  * You have a single Active Directory forest on-premises
  * You have an enterprise administrator account you can use for the installation
  * You have less than 100,000 objects in your on-premises Active Directory
  * You want to enable **Password Hash Synchronization** by default

**Note**: If you don't satisfy any of the above requirements, choose the **Custom** install option. We do advise that you use the default installation when possible, allowing **Azure AD Connect** to create accounts instead of providing your own accounts. Custom accounts must be configured precisely to provide necessary permissions, which, if done in error, may result in synchronization problems. 

* Please [setup a backup server in staging mode](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-operations), which will be used as a fallback server in case your primary server goes down. Ensure the staging server is configured the same as the primary server. Whenever you make any configuration changes on primary server, please ensure to make same settings on staging server also.

### **Upgrade from previous version**

It is highly recommended to keep your **Azure AD Connect** updated to latest version. **Azure AD Connect** auto upgrade works in most of cases except for following:

* If you have customized your synchronization rules
* If you are using remote SQL database
* If your configuration is in bad state
* If you have not configured your sign in method or configured it as **Pass Through Authentication**
* If your local database has exceeded it's size limit of 10GB
* If you have disabled AAD Connect Health Agent
* If you have intentionally disabled auto upgrade

In the case auto upgrade is not working for you due to any reason above, you can [download the latest version of **Azure AD Connect**](https://www.microsoft.com/download/details.aspx?id=47594). Launch AzureADConnect.msi and follow wizard instructions to complete the upgrade. Don't forget to upgrade your staging server as well as the primary server.

### **Common Issues**

* [Connectivity issues with on-premise Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
* [Connectivity issues with online Azure Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity)
* [Permission issues with on-premise Active Directory](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account)

## **Recommended Documents**

* [Prerequisites for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-prerequisites)
* [Select which installation type to use for Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-select-installation)
* [Getting started with Azure AD Connect using express settings](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express)
* [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-custom)
* [Azure AD Connect: Upgrade from a previous version to the latest](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-upgrade-previous-version)
* [Azure AD Connect: What is staging server?](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-topologies#staging-server)
* [What is the ADConnectivityTool PowerShell Module?](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)
