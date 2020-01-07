<properties
    pageTitle="Mobility agent configuration failed because of RCM connectivity issue"
    description="Mobility agent configuration failed because of RCM connectivity issue"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_MobilityAgentConfigurationFailure_NoConnectivityToRcmIps"
    diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public"
/>

# Mobility agent configuration failed because of RCM connectivity issue

<!--issueDescription-->
Installation of Mobility agent failed with error **A2AMobilityServiceConfiguratorConfigurationFailedWithNoConnectivityToRcmIps**. Connection can’t be established to Azure Site Recovery service endpoints.
<!--/issueDescription-->

## **Recommended Steps**

Make sure communication with the prerequisite URLs or datacenter IP ranges is allowed when using Azure Network security group (NSG) rules or a firewall proxy to control outbound network connectivity on the virtual machine,  Refer to [Site Recovery configuration failed (151197)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#issue-3-site-recovery-configuration-failed-151197).
