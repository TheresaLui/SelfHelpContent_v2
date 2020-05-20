<properties
    pageTitle="Push installation fails because logon servers are not available on source machine"
    description="Push installation of mobility agent fails because logon servers are not available on source machine while copying the mobility agent software to the source machine."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_LogonServersNotAvailable"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails because logon servers are not available on Source Machine

<!--issueDescription-->
Push installation failed as logon servers are not available on the source machine to accept the login request. Login service might not be running on the source machine or the service is listening at a different port.
<!--/issueDescription-->

## **Recommended Steps**

1. After making sure that the Logon servers are available on the source machine, start the logon service with the command `net start Netlogon`, or start "NetLogon" from the Task Manager
2. Check the following points before proceeding further:

    - Ensure you are using valid credentials with administrative privileges. For more information, see [Credentials check (ErrorID: 95107 & 95108)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108).
    - [Enable file & print sharing](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
    - [Enable WMI](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103)
    
3. **OR** Install mobility agent on the source machine through [simple manual installation process](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#install-mobility-service-manually-by-using-the-gui) or by using software deployment tool like [SCCM](https://docs.microsoft.com/azure/site-recovery/vmware-azure-mobility-install-configuration-mgr)
