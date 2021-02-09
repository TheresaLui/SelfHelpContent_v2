<properties
	pageTitle="UserErrorGuestAgentVersionUnsupported"
	description="UserErrorGuestAgentVersionUnsupported"
	infoBubbleText="Linux backup operation might have failed, because of an unsupported Guest Agent version on the VM"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorguestagentversionunsupported"
	diagnosticScenario="azurebackup-crc-usererrorguestagentversionunsupported"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorGuestAgentVersionUnsupported

<!--issueDescription-->
We have identified that your Linux backup operation might have failed, because of an unsupported Guest Agent version on the VM.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue:

- Ensure the Linux VM Guest Agent is of [supported version](https://support.microsoft.com/help/4049215/extensions-and-virtual-machine-agent-minimum-version-support)
- Follow the steps listed in this [article](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent) to upgrade the Guest Agent to latest version
