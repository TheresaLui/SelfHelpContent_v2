<properties
pageTitle="Agent installed is below minimum version"
description="Agent installed is below minimum version"
infoBubbleText="Agent installed is below minimum version"
service="microsoft.compute"
resource="virtualmachines"
authors="scottAzure"
displayOrder=""
articleId="Agent_validateagentminversion"
diagnosticScenario="Agent installed is below minimum version"
selfHelpType="diagnostics"
supportTopicIds="32411845"
resourceTags=""
productPesIds="14749,15797,15571"
cloudEnvironments="public"
/>

# Agent installed is below minimum supported version
<!--issueDescription-->
We have detected that the Agent installed for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** is below the minimum supported version for **<!--$ostype-->OS Type<!--/$ostype-->**:
* Detected version **<!--$agentversioninstalled-->Agent version<!--/$agentversioninstalled-->**
* Minumum supported version **<!--$agentversionminimum-->Agent minimum version<!--/$agentversionminimum-->**
<!--/issueDescription-->

The installed version of the agent is below the required minimum version for the VM to run in Azure. Please upgrade the agent version installed on this virtual machine. Microsoft also recommends updating any custom images that may be used in future deployments to avoid this issue.<br>

For additional information regarding minimum agent version and how to upgrade:<br>
* [Minimum version support for virtual machine agents in Azure](https://support.microsoft.com/help/4049215/extensions-and-virtual-machine-agent-minimum-version-support)<br>
* [Upgrade the Linux Agent](https://docs.microsoft.com/azure/virtual-machines/linux/update-agent)<br>
* [Upgrade the Windows Agent](https://docs.microsoft.com/azure/virtual-machines/windows/agent-user-guide)
