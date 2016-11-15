<properties
	pageTitle="Site Recovery (VMware to Azure)/Replication does not progress"
	description="Site Recovery (VMware to Azure)/Common issues during replication"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536441"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Site Recovery (VMware to Azure)/Replication does not progress

Common issues during replication

**Slow replication  / Data upload throttled**

If you see the replication pairs are progressing slowly then please make sure you have the sufficient  bandwidth.

- Use [ASR capacity planner](http://aka.ms/azure-site-recovery-capacity-planner-guidelinesLink) to calculate the bandwidth required for replication 

- You can [configure the upload thread limit](https://azure.microsoft.com/en-in/documentation/articles/site-recovery-vmware-to-azure/#network-bandwidth-considerations) to influence the bandwidth traffic. 

**Replication Stuck**

- Make sure that source machines are able to communicate with configuration server which means inbound 443 port on configuration server is not blocked. Please check [configuration server prerequisite](https://aka.ms/selfhelp_csprereqs) for more details 
- Please make sure that you are following [anti virus recommendation](https://support.microsoft.com/en-in/kb/3186955) for ASR.
 

**Data upload Blocked**


* Ensure that the network connectivity exists between the source machine and the process server
- In case of VPN connection please ensure the connectivity
- Check to see if the mobility service (InMage Scout VX Agent - Sentinel/Outpost, InMage Scout Application Service) is running on the source server

## **Recommended  Documents**
[VMware to Azure](aka.ms/asrstv2a)
