<properties
    articleid="72da7dea-2f8d-4127-996f-fc699a862139"
    pageTitle="Sync issues: Connector account"
    description="Sync issues: Connector account"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629772"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public"
    />

# Sync issues: Connector account

## **Recommended steps**
For an overview of the different accounts used by Azure AD Connect see this guide [Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions).

### **AD DS Connector account**

* This account is used to read/write information to Windows Server Active Directory. 

* If you have changed, or want to change the password of this account see this guide [Changing the AD DS account Password](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-change-addsacct-pass).

* **Permissions Issues:** A common issue is that this account does not have the required permissions on AD DS. See this guide [AD DS Connector Account Permissions](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account) to learn how to apply the required permissions. 

* **Best Practice** is to allow the **Azure AD Connect** wizard to auto create this account during installation. Auto creating this account will ensure that this account is configured with the required permissions. [More details on the AD DS Connector account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions). 

### **Azure AD Connector account**

* This account is used to read/write information to Azure AD.

* To change the password of this account see this guide [How to manage the Azure AD service account](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-azureadaccount).

* **Best Practice** is to allow the Azure AD Connect wizard to create this account during installation.

* There is a limit on the number of these accounts that can be created – this limit can sometimes be hit when installing/uninstalling Azure AD Connect multiple times. This guide [More details on the Azure AD Connector account](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions) explains how to address this by removing unused accounts.


## **Recommended documents**
* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Azure AD Connect: Configure AD DS Connector Account Permissions](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-configure-ad-ds-connector-account)
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)
* [Changing the AD DS account password](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-change-addsacct-pass)
* [Azure AD Connect sync: How to manage the Azure AD service account](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-azureadaccount)
* [Troubleshoot SQL connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-tshoot-sql-connectivity)
