<properties
pageTitle="Ensure listening port and open NSG to allow source IP"
description="Ensure listening port and open NSG to allow source IP"
infoBubbleText= "Issues with your Load Balancer Backend Pool Connectivity were detected. See details on the right."
service="microsoft.network"
resource="loadBalancers"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="3350c353-0ab0-42e0-8c2e-356100b87d71"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32588977"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_LoadBalancer"
/>

# Ensure listening port and open NSG to allow source IP

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your load balancer backend pool connectivity issue. We’ve reviewed diagnostics and configuration available to us and have determined that your connectivity issue is likely due to either a) the NSG is not configured to allow the destination port on the backend pool b) there is no application running and listening on the destination port expected/configured for the backend pool. Please take necessary steps to correct this configuration to resolve your connectivity issue. If you need additional support on this matter, please let us know.  

Best regards,
<!--/issueDescription-->