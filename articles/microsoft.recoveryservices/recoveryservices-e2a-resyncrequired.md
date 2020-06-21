<properties
	pageTitle="Resynchronization required for the protected virtual machine"
	description="E2A resynch required for VM"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536449"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="5d3c0952-aa52-4c85-b2e7-41b48ab327b5"
	ownershipId="Compute_SiteRecovery"
/>
# 'Resynchronization required' on the protected virtual machine

A VM is marked for resynchronization if delta replication fails and a full replication is costly in terms of bandwidth or time. For example, if the .hrl files reach 50% of the disk size, the VM is marked for resynchronization. By default, resynchronization is scheduled to run automatically outside office hours.

After resynchronization finishes, normal delta replication resumes.

## **Recommended Documents**

- The **Resynchronization process section** of [Hyper-V to Azure disaster recovery architecture](https://docs.microsoft.com/azure/site-recovery/concepts-hyper-v-to-azure-architecture#resynchronization-process) explains what resynchronization is and why is it needed<br>
- [Deployment planner recommendations](https://docs.microsoft.com/azure/site-recovery/site-recovery-hyper-v-deployment-planner)<br>
