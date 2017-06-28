.<properties
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

## **Recommended Steps**

**Slow replication  / Data upload throttled**

If you see the replication pairs are progressing slowly then please make sure you have the sufficient  bandwidth.

- **Cache folder exceeding threshold** alert means default threshold limit on process server cache for replication is being hit.This is common during initial replication or during high churn and it should goes away if there is sufficient bandwidth.
- Use [ASR capacity planner](https://aka.ms/asr-capacity-planner-doc) to calculate the bandwidth required for replication 
- [Configure max upload thread limit](https://aka.ms/max-thread-upload) to influence the bandwidth traffic. 

**Replication Stuck**

- Make sure that inbound port 443 on configuration server is not blocked. It can be checked using telnet. [Read for more details about configuration server prerequisite](https://aka.ms/selfhelp_csprereqs) 
- Make sure that you are following [anti virus recommendation](https://aka.ms/asr-antivirus) for ASR.
- In case of bytes read error, ensure that any sector on the source disk is not corrupt by running chkdsk (dd for linux) in read-only mode. After fixing errors with chkdsk disable/enable protection. 
- Make sure you are not protecting a cloned server.
- Make sure that proxy if any is correctly set up

**Data upload Blocked**

* Ensure that the network connectivity exists between the source machine and the process server
- In case of VPN connection please ensure the connectivity.
- Check to see if the mobility service (InMage Scout VX Agent - Sentinel/Outpost, InMage Scout Application Service) is running on the source server

## **Recommended  Documents**
[VMware to Azure](http://aka.ms/asrstv2a)
