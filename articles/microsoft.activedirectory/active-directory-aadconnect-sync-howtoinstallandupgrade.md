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
    cloudEnvironments="public"
    />

# Azure AD Connect install and upgrade

## **Recommended Steps**
For simplicity sake we have provided limited information as best practices here, for more advanced information you can go through [**Reccommended Documents**](#recommended-documents):

### **Clean Install**

* [Download latest version of **Azure AD Connect**](https://www.microsoft.com/download/details.aspx?id=47594) and launch AzureADConnect.msi on the server where you want to install it.

* It is advised to install **Azure AD Connect** on a dedicated server. 

* Please ensure you are logged in as Administrator on the server you are installing **Azure AD Connect**.

* Select **Express** installation with default options if you meet following requirements.

  * You have a single Active Directory forest on-premises.
  * You have an enterprise administrator account you can use for the installation.
  * You have less than 100,000 objects in your on-premises Active Directory.
  * You want to enable **Password Hash Synchronization** by default.

* If you don't satisfy any of the above requirements then you can go ahead with **Custom** install option. However go with default options as much as possible and let **Azure AD Connect** create various accounts instead of providing your own accounts. The issue with providing your own accounts is that you need to configure these accounts to provide necessary permissions, if not configured properly may result in synchronization issues. In contrast if **Azure AD Connect** create those accounts for you then it ensures to configure them properly to provide correct set of permissions.

* Please [setup a backup server in staging mode](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-operations), you can use this fallback server in case your primary server goes down. Please ensure to configure staging sever same as primary server with same settings. Whenever you make any configuration changes on primary server, please ensure to make same settings on staging server also.

### **Upgrade from previous version**

It is highly recommended to keep your **Azure AD Connect** updated to latest version. **Azure AD Connect** auto upgrade works in most of cases except for following:

* If you have customized your synchronization rules.

* If you are using remote SQL database. 

* If your configuration is in bad state.

* If you have not configured your sign in method or configured it as **Pass Through Authentication**.

* If your local database has exceeded it's size limit of 10GB.

* If you have disabled AAD Connect Health Agent.

* If you have intentionally disabled auto upgrade.

In case auto upgrade is not working for you because of any of above option then you can [download latest version of **Azure AD Connect**](https://www.microsoft.com/download/details.aspx?id=47594) and launch AzureADConnect.msi and follow wizard instructions to upgrade it. Please ensure to upgrade the staging server also if you have setup one.

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