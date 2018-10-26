<properties
    pageTitle="Azure Stack Patch and Update Management"
    description="Assist customers before and during patch and update runs"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567910, 32567944"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack Patch and Update Management

## **Recommended steps**

### **Availability of Updates**

Customers with Azure Stack environments connected to the internet will automatically see "Update Available" in the Admin Portal. For disconnected customers, update releases notifications are available vis RSS feed at [Support Content Updates](https://support.microsoft.com/en-us/help/4089498/support-content-updates), select Product as *Azure Stack* and choose ATOM or RSS.

### **If you are preparing to apply an Azure Stack update:**

1. Check the release notes for the latest package, listed under [Update Package Release Cadence](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)<br>
2. Perform a pre-check on the health of your environment by running Test-AzureStack according to the steps under [Plan for Updates](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-updates#plan-for-updates).<br>

```PowerShell
Test-AzureStack -Include AzsControlPlane, AzsDefenderSummary, AzsHostingInfraSummary, AzsHostingInfraUtilization, AzsInfraCapacity, AzsInfraRoleSummary, AzsPortalAPISummary, AzsSFRoleSummary, AzsStampBMCSummary
```

3. Resolve any operational issues found in Test-AzureStack output, including all warnings and failures. Also review active alerts, and resolve any that require action.

### **If you are monitoring an on-going update run:**

Check the status of the update using the steps to [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/azure/azure-stack/azure-stack-monitor-update#use-the-update-management-cmdlets)<br>

## **Recommended documents**

* [Azure Stack servicing policy - Recent Update](https://docs.microsoft.com/azure/azure-stack/azure-stack-servicing-policy#update-package-release-cadence)<br>
* [Manage updates in Azure Stack overview](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)<br>
* [Monitor updates in Azure Stack using the privileged endpoint](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-monitor-update)<br>