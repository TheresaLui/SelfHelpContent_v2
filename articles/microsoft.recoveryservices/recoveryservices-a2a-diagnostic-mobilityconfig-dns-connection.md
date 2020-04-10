<properties
    pageTitle="Mobility agent configuration failed because of DNS issue"
    description="Mobility agent configuration failed because of DNS issue"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_MobilityAgentConfigurationFailure_DNSConnectionFailure"
    diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility agent configuration failed because of DNS issue

<!--issueDescription-->
Installation of Mobility agent failed with error **A2AMobilityServiceConfiguratorConfigurationFailedWithDNSissue**. The connection can’t be established with the site recovery endpoints because of a DNS resolution failure.
<!--/issueDescription-->

## **Recommended Steps**

Make sure the DNS resolution is working on the virtual machine. Refer to [Failed to register Azure virtual machine with Site Recovery](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#issue-1-failed-to-register-azure-virtual-machine-with-site-recovery-151195-br)
