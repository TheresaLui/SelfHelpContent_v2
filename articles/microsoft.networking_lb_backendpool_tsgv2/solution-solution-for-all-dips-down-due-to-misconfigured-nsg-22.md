<properties
	  pageTitle="Solution for All DIPs down due to misconfigured NSG"
	  description="Solution for All DIPs down due to misconfigured NSG"
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
	  articleId="79ac4f6a-6af0-4423-acdb-eb1dad2e2945"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution for All DIPs down due to misconfigured NSG

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer backend pool connectivity issue. We have reviewed diagnostics and configuration available to us and have determined that your connectivity issue is likely due to a misconfiguration with the NSG applied to your backend VM. Please ensure that traffic from the IP address 168.63.129.16 is allowed inbound to your VM. This can be done by adding an inbound rule with higher priority (lower number) than your block rules to allow traffic from source tag AzureLoadBalancer to the probe port configured. Please see documentation https://docs.microsoft.com/azure/virtual-network/what-is-ip-address-168-63-129-16 and https://docs.microsoft.com/azure/virtual-network/service-tags-overview for more information.

If you need additional support on this matter, please let us know.  

Best regards,

<!--/issueDescription-->

