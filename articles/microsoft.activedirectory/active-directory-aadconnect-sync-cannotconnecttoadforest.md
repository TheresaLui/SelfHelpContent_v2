<properties
    pageTitle="Issues Connecting to AD Forest"
    description="Issues Connecting to AD Forest"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629771"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public"
    />

# Issues connecting to AD forest

## **Recommended steps**
If you see an error in the Azure AD Connect wizard when connecting to an AD forest then please go through following steps to troubleshoot and resolve it:

* Please check if you are running [latest version of AADConnect](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-version-history). Recent builds of Azure AD Connect automatically runs an AD connectivity troubleshooting script which will give more specific error details in the wizard. 

* You can run the AD connectivity troubleshooting script manually by opening a powershell command prompt and running “import-module C:\Program Files\Microsoft Azure Active Directory Connect\Tools\ADConnectivityTool.psm1", then calling “Start-ConnectivityValidation”. More details can be found here [AD Connectivity Tool Overview](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools) and here [AD Connectivity Tool Reference](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools). 

* When configuring an AD Forest, the Azure AD Connect wizard enumerates all the child domains under the selected forest. If there is an issue reaching any one of them then you may see this failure: “The specified domain/forest either does not exist or could not be contacted”. 

* This problem can occur if a domain controller in the domain has not registered an "A" record for itself in DNS. Resolution is to add the A record for the domain controller with the ipconfig /registerdns command. Flush the DNS cache on the computer running the Active Directory Installation Wizard by using the ipconfig /flushdns command. 

* You can use [Troubleshooting Active Directory Related DNS Problems](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-2000-server/bb727055%28v%3dtechnet.10%29) guide to troubleshoot DNS issues.

## **Recommended documents**
* [What is the ADConnectivityTool PowerShell Module?](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-adconnectivitytools)
* [Azure AD Connect: ADConnectivityTools PowerShell Reference](https://docs.microsoft.com/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
* [Troubleshooting Active Directory Installation Wizard Problems](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-2000-server/bb727058%28v%3technet.10%29)
* [Troubleshooting Active Directory—Related DNS Problems](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-2000-server/bb727055%28v%3dtechnet.10%29)