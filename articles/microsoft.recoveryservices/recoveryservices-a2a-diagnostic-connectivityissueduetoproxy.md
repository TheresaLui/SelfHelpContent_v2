<properties
	pageTitle="Microsoft Azure has information regarding your issue"
	description="Microsoft Azure has information regarding your issue"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details on the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	ms.author="asgang,genli"
	displayOrder=""
	articleId="vmnotconnectingduetoProxy"
	diagnosticScenario="ASRA2AMobilityAgentConfiguratorFailure"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Your virtual machine is not able to access "login.microsoftonline.com" due to invalid proxy. 
<!--issueDescription-->
The installation of Mobility service has failed with error **A2AMobilityServiceConfiguratorConfigurationFailed**. The connection to Azure Active Directory (AAD) cannot be established. The problem may occur if the network traffic goes through the proxy server and the proxy settings in the virtual machine is invalid.
<!--/issueDescription-->

## **Recommended Steps**

1. Make sure that the proxy setting is set correctly in the virtual machine. The Mobility Service auto detect the proxy settings in the following places:

	- For Windows: The **Proxy server** settings in Internet Explorer
	- For Linux: /etc/environment

2. If you prefer to set proxy only for the Mobility service, you can provide the proxy details in **ProxyInfo.conf** that is located in:

	- For Windows: C:\ProgramData\Microsoft Azure Site Recovery\Config
	- For Linux: /usr/local/InMage/config/ 

    The ProxyInfo.conf should have the proxy settings in the following INI format:

	```
	[proxy]
	Address=<proxy server url>
	Port=<port number>
	```
3. Azure Site Recovery Mobility Service agent supports only un-authenticated proxies
4. Refer to this troubleshooting [article](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#issue-4-a2a-replication-failed-when-the-network-traffic-goes-through-on-premises-proxy-server-151072) to resolve the issue

## **Recommended Documents**

* [Azure VM disaster Recovery connectivity requirements](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking#outbound-connectivity-for-ip-address-ranges)
* Learn more about troubleshooting [connectivity failures](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#issue-4-a2a-replication-failed-when-the-network-traffic-goes-through-on-premises-proxy-server-151072)
