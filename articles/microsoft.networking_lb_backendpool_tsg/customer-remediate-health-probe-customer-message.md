<properties
pageTitle="NSG is not allowing backend pool health probes"
description="NSG is not allowing backend pool health probes"
infoBubbleText= "Issues with your Load Balancer Backend Pool Connectivity were detected. See details on the right."
service="microsoft.network"
resource="loadBalancers"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="e5487bd2-7bd6-4140-9f88-3739c255b463"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds="32588977"
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_LoadBalancer"
/>

# NSG is not allowing backend pool health probes

<!--issueDescription-->
Dear customer,

Thank you for contacting us about your load balancer backend pool connectivity issue. We’ve reviewed your configuration and have determined that your connectivity issue is because backend pool health probes from the load balancer are being blocked by an NSG. To remediate this issue, please configure your NSG to allow health probes from 168.63.129.16.

Best regards,
<!--/issueDescription-->