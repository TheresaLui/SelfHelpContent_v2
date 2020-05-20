<properties
    pageTitle="Push installation of mobility agent fails with primary domain and workstation trust failure"
    description="Push installation of mobility agent fails because the credentials provided for push installation do not correspond to the primary domain configured on the source machine."
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_V2A_PushInstallFailure_PrimaryDomainWorkstationTrustFailure"
    diagnosticScenario="ASRV2APushInstallFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Push installation of mobility agent fails with primary domain and workstation trust failure

<!--issueDescription-->
The credentials provided for push installation do not correspond to the primary domain configured on the source machine when push install service tries to copy the mobility agent software to the source machine from scale-out process server or configuration server.
<!--/issueDescription-->

## **Recommended Steps**

1. Ensure that the credentials provided under the user account (%AccountName;) have administrator privileges to log in to primary domain of the source machine (%SourceIP;). For detailed instructions, see [Credentials check (ErrorID: 95107 & 95108)](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#credentials-check-errorid-95107--95108).
2. Check the following points before proceeding further:

    - [Enable file & print sharing](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#file-and-printer-sharing-services-check-errorid-95105--95106)
    - [Enable WMI](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#windows-management-instrumentation-wmi-configuration-check-error-code-95103)
3. **OR** Install mobility agent on the source machine through [simple manual installation process](https://docs.microsoft.com/azure/site-recovery/vmware-azure-install-mobility-service#install-mobility-service-manually-by-using-the-gui) or by using a software deployment tool like [SCCM](https://docs.microsoft.com/azure/site-recovery/vmware-azure-mobility-install-configuration-mgr)
