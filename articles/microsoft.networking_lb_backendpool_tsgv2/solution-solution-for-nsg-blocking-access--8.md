<properties
	  pageTitle="Solution for NSG blocking access."
	  description="Solution for NSG blocking access."
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
	  articleId="9e2b1fda-57ec-4394-9d4d-b062b9ef4f83"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution for NSG blocking access.

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer connectivity issue. We have noticed that NSG rule <rule name> is blocking traffic. Please remedy this by adding a lower rule with a lower number rule priority allowing the traffic. You can test this using the Network Watcher IP Flow Verify tool in the Azure Portal.

For more information, see: https://docs.microsoft.com/azure/virtual-network/diagnose-network-traffic-filter-problem and https://docs.microsoft.com/azure/network-watcher/network-watcher-ip-flow-verify-overview.


Thank you,

<!--/issueDescription-->

