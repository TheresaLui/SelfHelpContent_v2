<properties  
	pageTitle="I can't connect to my Windows VM"
	description="I can't connect to my Windows VM"
	service=""
	resource=""
	authors="manavis"
	displayOrder="30"
	selfHelpType="generic"
	supportTopicIds="32615526"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public"
/>

# I can't connect to my Windows VM

## **Recommended documents**

1. Troubleshoot common [RDP connection issues](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-rdp-connection)
2. Troubleshoot connectivity issues using [Network Watcher connection troubleshoot](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.sourceId.$resourceId) when trying RDP from Azure
3. Review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId) to ensure inbound “Allow” NSG rule exists and is prioritized for RDP port(default 3389)
4. [Serial Console guide](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/serial-console-windows)
