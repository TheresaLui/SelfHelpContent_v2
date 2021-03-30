<properties
    pageTitle="Synchronization does not work at all"
    description="Synchronization does not work at all"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32684521"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="dea86da8-dd32-4842-865e-51178310350d"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Synchronization does not work at all

Use this article to resolve issues with synchronization failures in Azure Active Directory (AAD) Connect.

## **Recommended Steps**

When synchronization stops working, it can generate issues with installation, and with accounts and permissions used by the synchronization services.

- For **installation issues with Azure AD Connect**, go back to the previous page, and select "I have a problem installing or uninstalling AADConnect" as the support sub-topic to see common solutions for installation issues. 

**Important:** If you use a **deprecated version of sync, such as DirSync or AADSync**, be aware that these versions will **stop working on April 1st, 2021**. Refer to [the docunmentation on DirSync deprecation and how to upgrade to AAD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-dirsync-upgrade-get-started)

For all Azure AD Connect sync issues that aren't related to installation, see the next section to troubleshoot and resolve your issue.

### Synchronization Service won't start in Windows Service Control Manager

Common root causes include the following:

* The Azure AD Connect sync service account, which is used by the Synchronization Service as its security context, recently changed its password. To resolve this issue, refer to [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass).

* The Azure AD Connect sync service account has not been granted [**Log on as a Service**](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/log-on-as-a-service) rights

* The Azure AD Connect server is using **LocalDB** as its database, which has a 10 GB limit. When using LocalDB and this limit is reached, the Synchronization Service can no longer start or synchronize properly. To recover from this issue, refer to [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).


### Issues connecting Azure AD Connect server to your domains or forests

For errors in the Azure AD Connect wizard when connecting to an AD forest, review the following items to troubleshoot and resolve it.

* **Run the [latest version of AAD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-version-history)** 
   Recent builds automatically run an AD connectivity troubleshooting script that give you specific error details in the wizard. 
     * To run the AD connectivity troubleshooting script manually, open a PowerShell command prompt and run `import-module C:\Program Files\Microsoft Azure Active Directory Connect\Tools\ADConnectivityTool.psm1`. Then, call `Start-ConnectivityValidation`. 

* **Specified domain/forest doesn't exist**
   When configuring an AD Forest, the Azure AD Connect wizard enumerates all the child domains under the selected forest. If there's an issue reaching any one of them, you may see this error: "The specified domain/forest either does not exist or could not be contacted".   
    This problem can occur if a domain controller in the domain has not registered an "A" record for itself in DNS. Resolution is to add the A record for the domain controller with the `ipconfig /registerdns` command. Flush the DNS cache on the computer running the Active Directory Installation Wizard with `ipconfig /flushdns`.

* **DNS issues**
  If you're encountering DNS issues, use this guide [Troubleshooting Active Directory Related DNS Problems](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-2000-server/bb727055%28v%3dtechnet.10%29).

### Problems connecting Azure AD Connect server to a SQL server

If you see a problem related to the connectivity between your Azure AD Connect server and your SQL server, please follow the troubleshooting steps as described in [Troubleshooting SQL Server Connectivity](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-tshoot-sql-connectivity).

### Problems connecting Azure AD Connect server to Azure AD

If you see a problem which may be related to the connectivity between your Azure AD Connect server and Azure AD, please follow the troubleshooting steps as described in [Troubleshooting Azure AD connectivity](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity). 

### Problems with Azure AD Connect sync cycle execution
   The synchronization cycle has three steps: import, export, and synchronization. Import or export errors can lead to synchronization errors.

### Synchronization Issues
   Use a [troubleshooting script](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync) to troubleshoot object synchronization with Azure AD Connect sync


### Import Issues

There can be several reasons why an object won't import:

* **AD connectivity issues**: Use [ADConnectivityTools](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools) to check connectivity issues with on premise AD
* **Azure AD connectivity issues**: Follow instructions to [troubleshoot connectivity issues with Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-connectivity)
* **AD permissions issues**: As a best practice to avoid any permission issues, let Azure AD Connect [create accounts instead of providing custom accounts](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* **Scoping issue**: The object belongs to a [domain or OU which is filtered out](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-configure-filtering) or there is sync rule to filter out the object


### Export Issues

* **Data mismatch issue**: [Could not find mapping object](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#data-mismatch-errors)
* **Duplicate attributes**: [Azure AD expects some attributes to be unique for each object](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#duplicate-attributes)
* **Data validation failures**: [Azure Active Directory enforces various restrictions on the data](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#data-validation-failures)
* **Large object failures**: [Azure Active Directory restricts size limit for some attributes](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#largeobject)
* **Existing admin role conflict**: [Azure AD restricts some users from being synced if these users have already existin Azure AD and have an administrative roles assigned to them](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors#existing-admin-role-conflict)

### Other Issues

* For advanced troubleshooting, [review how objects flow in AAD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing)

## **Recommended Documents**

* [Azure AD Connect: Accounts and permissions](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-accounts-permissions)
* [Changing the Azure AD Connect sync service account password](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-change-serviceacct-pass)  
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)
* [Table-valued parameter errors after AADConnect is installed on Windows Server 2019](https://docs.microsoft.com/troubleshoot/azure/active-directory/tvp-errors-when-aadconnect-installed-on-windows-server-2019)
