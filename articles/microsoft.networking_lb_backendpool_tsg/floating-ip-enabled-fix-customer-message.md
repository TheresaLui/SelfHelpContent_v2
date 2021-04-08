<properties
pageTitle="Disable or correct the Floating IP configuration"
description="Disable or correct the Floating IP configuration"
infoBubbleText= "Issues with your Load Balancer Backend Pool Connectivity were detected. See details on the right."
service="microsoft.network"
resource="loadBalancers"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="712dd4cc-d346-4f7e-8743-4c4bb99ba9d8"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32588977"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_LoadBalancer"
/>

# Disable or correct the Floating IP configuration 

<!--issueDescription-->
Dear Customer,

Thank you for contacting us about your load balancer backend pool connectivity issue. We’ve reviewed the logs and diagnostics available to us and we believe the connectivity issue you’re experiencing may be the result of specifying floating IP on your load balancing rule. Backend connectivity may not work if your VM is not configured to accept connections for the frontend IP address of your load balancing rule. Typically, this is done in conjunction with a clustering technology such as Windows Clustering. You can also do this by configuring a loopback adapter in your OS. For more information, see [this documentation](https://docs.microsoft.com/azure/load-balancer/load-balancer-floating-ip).

Best regards,
<!--/issueDescription-->
