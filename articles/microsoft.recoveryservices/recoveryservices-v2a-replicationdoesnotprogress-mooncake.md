<properties
	pageTitle="Site Recovery (VMware to Azure)/Replication does not progress"
	description="Site Recovery (VMware to Azure)/Common issues during replication"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder="11"
	selfHelpType="generic"
	supportTopicIds="32536441"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="MoonCake"
	articleId="e7973819-966a-43d6-b53d-2aa5a84cfc46"
/>

# Replication not progressing - VMware/Physical to Azure

## **Recommended documents**

* Troubleshoot [Initial replication issues](https://docs.azure.cn/site-recovery/vmware-azure-troubleshoot-replication/)
* Replication is stuck and not progressing? Follow this troubleshooting [article](https://docs.azure.cn/site-recovery/vmware-azure-troubleshoot-replication)
* Troubleshoot error message ['No application consistent recovery point available for the VM'](https://blogs.technet.microsoft.com/srinathv/2018/01/11/troubleshooting-no-latest-app-consistent-snapshot-issues-for-vmware-to-azure-when-using-azure-site-recovery/)
* VM is protected, but Replication health is critical? Check if current churn/bandwidth is meeting recommendations. Run the [Deployment planner](https://docs.azure.cn/site-recovery/site-recovery-vmware-deployment-planner-run) and review recommendations for [network](https://docs.azure.cn/site-recovery/site-recovery-vmware-deployment-planner-analyze-report#recommendations-with-available-bandwidth-as-input) and [storage](https://docs.azure.cn/site-recovery/site-recovery-vmware-deployment-planner-analyze-report#vm-storage-placement)
* Check if you need to adjust the bandwidth and throttling as listed in this [article](https://docs.azure.cn/site-recovery/site-recovery-plan-capacity-vmware#control-network-bandwidth)
