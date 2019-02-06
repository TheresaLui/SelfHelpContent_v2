<properties
	pageTitle="resynchronization required for the protected virtual machine? "
	description="H2A resynch required for VM"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536449"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>
# Are you seeing 'resynchronization required' on the protected virtual machine?

A VM is marked for resynchronization if delta replication fails and a full replication is costly in terms of bandwidth or time. For example, if the .hrl files reach 50% of the disk size, then the VM is marked for resynchronization. By default resynchronization is scheduled to run automatically outside office hours.

After resynchronization finishes, normal delta replication resumes.

## Want to know more?
- [What is resynchronization and why is it needed? How to do it?](https://docs.microsoft.com/azure/site-recovery/concepts-hyper-v-to-azure-architecture#resynchronization-process) <br>

## Want to avoid this in the future?

Follow our [Deployment planner recommendations](https://docs.microsoft.com/azure/site-recovery/site-recovery-hyper-v-deployment-planner) for a successful disaster recovery protection in Azure.<br>
