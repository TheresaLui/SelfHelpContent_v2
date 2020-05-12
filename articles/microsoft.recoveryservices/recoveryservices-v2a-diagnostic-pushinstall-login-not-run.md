<properties
    pageTitle="Push installation of mobility agent fails as login service not running"
    description="Push installation fails as login service is not running on the source machine to process the login request from process server."
    service="microsoft.recoveryservices"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_LoginServiceNotRunning"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails as login service not running

<!--issueDescription-->
Push installation fails as login service is not running on the source machine to process the login request from process server.
<!--/issueDescription-->

## **Recommended Steps**

1. Ensure that the Logon service is running on the source machine for successful login. To start the logon service, run the command `net start Netlogon` or start "NetLogon" from Task Manager.
2. Check the following points before proceeding further:

    - Ensure that you are using valid credentials with administrative privileges. For more information, see [Credentials check (ErrorID: 95107 & 95108)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108).
    - [Enable file & print sharing](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
    - [Enable WMI](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103)
3. **OR** Install mobility agent on the source machine through [simple manual installation process](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#install-mobility-service-manually-by-using-the-gui) or by using a software deployment tool like [SCCM](https://docs.microsoft.com/azure/site-recovery/vmware-azure-mobility-install-configuration-mgr)
