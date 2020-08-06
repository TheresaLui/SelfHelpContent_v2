<properties
pageTitle="Support for Basic Load Balancer only exists within the same region"
description="Support for Basic Load Balancer only exists within the same region"
infoBubbleText= "Issues with your Load Balancer Backend Pool Connectivity were detected. See details on the right."
service="microsoft.network"
resource="loadBalancers"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="d9f6b110-c613-4730-94f7-f72e8d01824f"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32588977"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_LoadBalancer"
/>

# Support for Basic Load Balancer only exists within the same region

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your load balancer backend pool connectivity issue. We’ve reviewed your configuration and we’ve determined your issue is due to the use of a basic load balancer. Resources in one virtual network cannot communicate with the front-end IP address of a basic internal load balancer in a globally peered vnet. Our suggestion at this time is to migrate your basic load balancer to a standard load balancer where this is a supported scenario. Here are the instructions of how to do it: https://docs.microsoft.com/azure/load-balancer/upgrade-basic-standard  

Best regards,
<!--/issueDescription-->
