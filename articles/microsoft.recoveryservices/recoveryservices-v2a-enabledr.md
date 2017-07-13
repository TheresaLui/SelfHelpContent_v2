<properties
	pageTitle="Site Recovery (VMware to Azure)/Enable Protection"
	description="Site Recovery (VMware to Azure)/Common issues during Enable Protection"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536405"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Can't Enable Replication? Initial Replication Failing?

**Most of our customers SELF-RESOLVED this issue by following this** **[Step-by-Step Troubleshooting guide](https://blogs.technet.microsoft.com/srinathv/2017/06/28/replication-stuck-replication-not-progressing/).**

The troubleshooting guide will help you identify issues related to:
* Connectivity issue between Source Server and Configuration/Process server
* Services status issues in Source/Process Server
* Process Server connectivity issues to Azure Public IP address using port 443
* IP based firewall on Process Server blocking access
* URL based firewall on Process Server blocking access
* Proxy Setting on Process Server blocking access
* Throttle Bandwidth settings on Process Server constraining replication
