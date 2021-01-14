<properties
	  pageTitle="Solution for All DIPs down during prior incident"
	  description="Solution for All DIPs down during prior incident"
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
	  articleId="abeba4d9-b76f-4124-b6a4-f52d578bf6e6"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution for All DIPs down during prior incident

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer connectivity issue on <insert date and time>. We have noticed that all members of the backend pool are detected as down by the load balancer probes. Please review any application logs and metrics you may have for more information.

To view metrics on your load balancer probe status, please browse to the load balancer object in the Azure Portal, click on the Metrics tab below Monitoring and select the Health Probe Status metric. We recommend using the Min aggregation and splitting on backend IP address and potentially port to see any changes in probe status over time. For more information, please see: https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-custom-probe-overview

Thank you,

<!--/issueDescription-->

