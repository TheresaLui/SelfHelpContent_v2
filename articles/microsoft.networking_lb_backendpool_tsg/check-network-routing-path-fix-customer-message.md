<properties
pageTitle="Add UDR for the BE pool subnet "
description="Add UDR for the BE pool subnet "
infoBubbleText= "Issues with your Load Balancer Backend Pool Connectivity were detected. See details on the right."
service="microsoft.network"
resource="loadBalancers"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="411d36f3-5621-4edb-baed-6658d3971575"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32588977"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_LoadBalancer"
/>

# Add UDR for the BE pool subnet

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your load balancer backend pool connectivity issue. We’ve reviewed your configuration and have determined that your connectivity issue is due to a missing UDR for the BE pool subnet. Please repair this issue by creating a UDR on the BE pool subnet with a route for 0.0.0.0/Internet

Best regards,
<!--/issueDescription-->