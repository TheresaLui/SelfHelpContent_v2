<properties
	pageTitle="Microsoft Azure has information regarding your issue"
	description="Microsoft Azure has information regarding your issue"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details to the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	ms.authoralias="asgang,genli"
	displayOrder=""
	articleId="vmnotconnectingtoO365IPs"
	diagnosticScenario="vmnotconnectingtoO365IPs"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public"
/>

# Your virtual machine is not able to access "login.microsoftonline.com".
<!--issueDescription-->
The installation of mobility service failed with error **A2AMobilityServiceConfiguratorConfigurationFailedWithNoConnectivityToOffice365Ips**. The connection to Office 365 authentication and identity IP4 endpoints cannot be established.
<!--/issueDescription-->

## **Recommended Steps**

1. Azure Site Recovery requires access to Office 365 IP ranges for authentication. You can log in to the virtual machine and check if you can access "https://login.microsoftonline.com".
2. If you are using Azure Network security group (NSG) rules or firewall proxy to control outbound network connectivity on the virtual machine, make sure that you allow communication to Office 365 IP ranges. To do this, create a **Azure Active Directory** [service tag](https://docs.microsoft.com/azure/virtual-network/security-overview#service-tags) based NSG rule for allowing access to all IP addresses corresponding to Azure Active Directory.
3. The virtual machine that behinds standard Internal loadblancer will face this problem because of outbound connectivity block. For more information, see [Outbound NAT for internal Standard Load Balancer scenarios](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-rules-overview#outbound-nat-for-internal-standard-load-balancer-scenarios
).

## **Recommended Documents**
* Learn more about [Azure VM disaster Recovery connectivity requirements](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking#outbound-connectivity-for-ip-address-ranges)
* Learn more about troubleshooting [connectivity failures](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-errors#outbound-connectivity-for-site-recovery-urls-or-ip-ranges-error-code-151037-or-151072)


