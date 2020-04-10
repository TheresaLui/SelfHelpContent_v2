<properties
    pageTitle="Push installation of mobility agent fails as root account is not provided in Linux VM"
    description="Push installation of mobility agent fails as root account is not provided in Linux VMs"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_LinuxNotRootAccount"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails because root account isn't provided in Linux VM

<!--issueDescription-->
The push installation of the mobility agent on Linux virtual machines fails because a built-in root account has not been provided.
<!--/issueDescription-->

## **Recommended Steps**

1. Verify that the account provided is built-in root user account and retry the operation
2. Check the following points before proceeding further:

    - Ensure that you are using valid credentials with administrative privileges. For detailed instructions, see [Credentials check (ErrorID: 95107 & 95108)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108).
    - [Enable file & print sharing](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
    - [Enable WMI](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103)

3. **OR** Install mobility agent on the source machine through [simple manual installation process](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#install-mobility-service-manually-by-using-the-gui) or by using a software deployment tool like [SCCM](https://docs.microsoft.com/azure/site-recovery/vmware-azure-mobility-install-configuration-mgr)
