<properties
pageTitle="Agent installed is below minimum version supported"
description="Agent installed is below minimum version supported"
infoBubbleText="Azure VM Agent installed is below minimum version supported"
service="microsoft.compute"
resource="virtualmachines"
authors="scottAzure"
displayOrder=""
articleId="agent_validateagentminversion"
diagnosticScenario="agentextensions"
selfHelpType="diagnostics"
supportTopicIds="32411845"
resourceTags=""
productPesIds="14749,15797,15571"
cloudEnvironments="public"
/>

# Azure VM Agent installed is below minimum supported version
<!--issueDescription-->
We have detected that the Azure VM Agent installed on your virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** is below the minimum supported version for **<!--$ostype-->OS Type<!--/$ostype-->**: Detected version **<!--$agentversioninstalled-->Agent version<!--/$agentversioninstalled-->**, Minimum supported version **<!--$agentversionminimum-->Agent minimum version<!--/$agentversionminimum-->**
<!--/issueDescription-->

The Microsoft Azure Virtual Machine Agent (VM Agent) is a secured, lightweight process that manages VM interaction with the Azure Fabric Controller. The VM Agent has a primary role in enabling and executing Azure virtual machine extensions.

The agent should be updated timely to receive fixes for the potential issues and to maintain compatibility with the Azure platform.

Detailed instructions to update the agent can be found here:
* [Upgrade the Linux Agent](https://docs.microsoft.com/azure/virtual-machines/linux/update-agent)
* [Upgrade the Windows Agent](https://docs.microsoft.com/azure/virtual-machines/windows/agent-user-guide)

Microsoft also recommends updating any custom images that may be used in future deployments to avoid this issue.<br>

## **Recommended Documents**
* [Minimum version support for virtual machine agents in Azure](https://support.microsoft.com/help/4049215/extensions-and-virtual-machine-agent-minimum-version-support)<br>
* [Azure Virtual Machine Agent for Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/agent-user-guide)
* [Azure Virtual Machine Agent for Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/agent-user-guide)
