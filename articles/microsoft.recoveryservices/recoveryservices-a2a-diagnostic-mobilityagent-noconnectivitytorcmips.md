<properties
    pageTitle="Mobility service Configuration failed due to connectivity issue to Site Recovery IP ranges"
    description="Mobility service Configuration failed due to connectivity issue to Site Recovery IP ranges"
    infoBubbleText="Some suggestions have been found to help solve your issue. Please see details to the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="genlin"
    ms.author="asgang"
    displayOrder=""
    articleId="ASR_A2A_MobilityAgentConfigurationFailure_NoConnectivityToRcmIps"
    diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility service Configuration failed due to AAD connectivity issue
<!--issueDescription-->
The installation of Mobility agent has failed because the connection cannot be established to Azure Site Recovery service endpoints.
<!--/issueDescription-->

## **Recommended Steps**

Azure Site Recovery required access to [Site Recovery IP ranges](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking#outbound-connectivity-for-ip-address-ranges) depending on the region. Make sure that required ip ranges are accessible from the virtual machine. To configure NSG rules for a VM to replicate, see [Example NSG configuration](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking#example-nsg-configuration).

## **Recommended Documents**

* Learn more about troubleshooting [connectivity failures](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#issue-1-failed-to-register-azure-virtual-machine-with-site-recovery-151195-br)
