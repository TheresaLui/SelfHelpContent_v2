<properties
	  pageTitle="Solution for All DIPs down due to NSG"
	  description="Solution for All DIPs down due to NSG"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="b9386683-08b0-4eab-a64d-d4f67a92c666"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution for All DIPs down due to NSG

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer connectivity issue. We have noticed that all members of the backend pool are detected as down by the load balancer probes. Please remedy this by ensuring:
1. The network service is properly running on the backend Virtual Machines and is listening on the port specified by the probe configuration. Use the ?netstat -ano? command to help validate this.
2. The guest OS firewall is allowing traffic to the port from the load balancer probe source IP address 168.63.129.16 as well as any other source IP addresses you wish to allow. For more information on the load balancer probe source IP address, please see: https://docs.microsoft.com/en-us/azure/virtual-network/what-is-ip-address-168-63-129-16

To view metrics on your load balancer probe status, please browse to the load balancer object in the Azure Portal, click on the Metrics tab below Monitoring and select the Health Probe Status metric. We recommend using the Min aggregation and splitting on backend IP address and potentially port to see any changes in probe status over time. For more information, please see: https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-custom-probe-overview

Thank you,

<!--/issueDescription-->

