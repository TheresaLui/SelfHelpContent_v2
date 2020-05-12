<properties
    pageTitle="Mobility agent configuration failed because of network connectivity issue"
    description="Mobility agent configuration failed because of network connectivity issue"
    infoBubbleText="Microsoft Azure has information regarding your issue. See details on the right."
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    articleId="ASR_A2A_MobilityAgentConfigurationFailure_NetworkConnectionFailure"
    diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Mobility agent configuration failed because of network connectivity issue

<!--issueDescription-->
Mobility agent configuration on host machine failed with error **A2AMobilityServiceConfiguratorRecoveryServiceConnectionFailed (ID: 151072)**.
<!--/issueDescription-->

## **Recommended Steps**

When using a firewall proxy or Azure Network security group (NSG) rules to control outbound network connectivity on the virtual machine, make sure communication with the prerequisite URLs or datacenter IP ranges is allowed. Refer to [A2A replication failed when the network traffic goes through on-premises proxy server (151072)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#issue-4-a2a-replication-failed-when-the-network-traffic-goes-through-on-premises-proxy-server-151072).
