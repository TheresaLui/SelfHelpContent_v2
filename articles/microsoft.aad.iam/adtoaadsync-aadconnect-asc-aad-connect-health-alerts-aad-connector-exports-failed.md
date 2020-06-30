<properties
    pageTitle="Export to Azure Active Directory failed"
    description="Export to Azure Active Directory failed"
    infoBubbleText="Export to Azure Active Directory failed See details on the right."
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder="1"
    articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_AAD_Connector_Exports_Failed"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>
# Export to Azure Active Directory failed

<!--issueDescription-->
Azure AD Connect was unable to export data to Windows Server Active Directory. As a result you may see error messages and/or unexpected synchronization results.
<!--/issueDescription-->

## **Recommended Steps**

To diagnose this issue, examine Windows Event Log for error events in the Application log. Look for error events that have "Directory Synchronization" as the Source in the Event Viewer. This will provide information about the exact nature of the export failure.
