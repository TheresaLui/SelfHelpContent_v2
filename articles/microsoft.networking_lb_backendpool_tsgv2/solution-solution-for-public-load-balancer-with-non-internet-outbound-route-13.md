<properties
	  pageTitle="Solution for public load balancer with non-internet outbound route"
	  description="Solution for public load balancer with non-internet outbound route"
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
	  articleId="1925c740-2866-4fa9-8d85-cce6460ce5c3"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution for public load balancer with non-internet outbound route

<!--issueDescription-->

## If rule name starts with: RouteTargetVpn

Dear <Customer>,

Thank you for contacting us about your public load balancer backend pool connectivity issue. We have reviewed the logs and diagnostics available to us and we determined the connectivity issue you are experiencing may be the result of a user defined route or default route being advertised from on-premises. To access your public load balancer from internet clients, it must not be on a Virtual Network subnet that is subject to a default route back to on-premises. We recommend you consult with your networking team to determine the appropriate next steps for your deployment and ensure it is consistent with any organizational policies you may have. For more information, see: https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview

Best regards,

## If rule name starts with: RouteTargetNva

Dear <Customer>,

Thank you for contacting us about your public load balancer backend pool connectivity issue. We have reviewed the logs and diagnostics available to us and we determined the connectivity issue you are experiencing may be the result of a user defined route to a network virtual appliance. To access your public load balancer from internet clients, it must not be on a Virtual Network subnet with a default route pointing to a network virtual appliance. We recommend you consult with your networking team to determine the appropriate next steps for your deployment and ensure it is consistent with any organizational policies you may have. For more information, see: https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview

Best regards,

<!--/issueDescription-->

