<properties
	pageTitle="Unable to connect to VM after fail over in A2A"
	description="Unable to connect to VM after fail over in A2A"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="v-bllydi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32574725"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Unable to connect to VM after fail over in A2A scenario
## **Recommended steps**
- [How to connect to a VM after failover to Azure?](https://docs.microsoft.com/azure/site-recovery/site-recovery-test-failover-to-azure#prepare-to-connect-to-azure-vms-after-failover)<br>
- **Connect button greyed out?** If the Connect button in the portal is dimmed, and you are not connected to Azure via an Express Route or Site-to-Site VPN connection, you need to create and assign your virtual machine a public IP address before you can use Remote Desktop/Shared Shell. You can then add a Public IP on the network interface of the virtual machine.[Details](https://docs.microsoft.com/azure/site-recovery/site-recovery-monitoring-and-troubleshooting#adding-a-public-ip-on-a-resource-manager-virtual-machine)<br>
- **Unable to RDP into the failed over VM?** [Use these troubleshooting steps](https://social.technet.microsoft.com/wiki/contents/articles/31666.troubleshooting-remote-desktop-connection-after-failover-using-asr.aspx)
