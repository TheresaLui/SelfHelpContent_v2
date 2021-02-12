<properties
    pageTitle="Connection to Azure Active Directory failed due to authentication failure"
    description="Connection to Azure Active Directory failed due to authentication failure"
    infoBubbleText="Connection to Azure Active Directory failed due to authentication failure See details on the right."
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder="1"
    articleId="ADtoAADSync_AADConnect_ASC_AAD_Connect_Health_Alerts_AAD_Authentication_Failure"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>

# Connection to Azure Active Directory failed due to authentication failure 
<!--issueDescription-->
Connection to Azure Active Directory failed due to authentication failure. As a result, objects will not be synchronized with Azure Active Directory. You should investigate and resolve this issue to resume synchronization with Azure Active Directory.
<!--/issueDescription-->

## **Recommended Steps**

To diagnose this issue, examine the Windows Event Log for error events in the Application log. Look for error events that have "Directory Synchronization" as the Source in the Event Viewer. This will provide information about the exact nature of the authentication failure.