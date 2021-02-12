<properties
	pageTitle="Check host high CPU"
	description="Check host high CPU"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c0de2891-ad44-42dd-b57b-e920d4d73b0d"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check host high CPU

1. To better understand if there is a high CPU utilization within the guest(VM) or on the host node we use the Hostanalyzer Report. For more information on how to run HostAnalyzer follow the TSG: [How to use ASC](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/266473/Azure_Virtual-Machine_Restart_HowTo_HowToUseASC)
2. High Host CPU utilization (to be found in tab "Host Metrics"/"Host Charts"), always look only at Hyper-V Root for Host CPU.
3. High Host CPU is demonstrated by Hypervisor Root Virtual Processor reaching ~100% utilization.
