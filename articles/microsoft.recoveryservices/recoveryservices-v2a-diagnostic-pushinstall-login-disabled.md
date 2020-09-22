<properties
    pageTitle="Push installation fails because login is disabled on source machine"
    description="Push installation of mobility agent fails because login is disabled on source machine while copying the mobility agent software to the source machine."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_LoginDisabledOnSourceMachine"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails because login is disabled on Source Machine

<!--issueDescription-->
The push install service is unable to copy the mobility agent software to the source machine from the scale-out process server or configuration server because the login credentials provided for the push installation have been **disabled** on the source machine.
<!--/issueDescription-->

## **Recommended Steps**

1. [Enable Login](https://docs.microsoft.com/powershell/module/microsoft.powershell.localaccounts/enable-localuser?view=powershell-5.1) on the source machine for the account provided or run this command in PowerShell: `net user 'username' /active:yes\`
2. Check the following points before proceeding further:

    - Ensure that you are using valid credentials with administrative privileges. For more information, see [Credentials check (ErrorID: 95107 & 95108)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108).
    - [Enable file & print sharing](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
    - [Enable WMI](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103)
    
3. **OR** Install mobility agent on the source machine through [simple manual installation process](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#install-mobility-service-manually-by-using-the-gui) or by using a software deployment tool like [SCCM](https://docs.microsoft.com/azure/site-recovery/vmware-azure-mobility-install-configuration-mgr)
