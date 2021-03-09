<properties
	pageTitle="Azure Load Balancer Management Issues - Health Probe Failures"
	description="Azure Load Balancer Management Issues - Health Probe Failures"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32781323"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6c"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer Health Probe Failures issues

## **Recommended Steps**

1.	Check if the backend is listening on the port that is configured on the health probe
2.	Check if the health probe is using the correct protocol. If you are using HTTP/HTTPS, confirm that the path is configured correctly.
3.	Make sure that service is listening on the IP address of the NIC’s IP configuration and not just on the loopback that’s configured with the front-end IP address.
4.	Check if the probe is permitted by the [Network Security Group](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group#view-details-of-a-network-security-group). You can also use the [Connection Troubleshoot](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal?WT.mc_id=Portal-Microsoft_Azure_Support#check-remote-endpoint-connectivity) feature on Network Watcher for this step.
5.	Check if the probe is permitted by VM’s guest OS firewall or other application layer filters.
