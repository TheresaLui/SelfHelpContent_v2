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
Dear customer,

Thank you for contacting us about your load balancer backend pool connectivity issue. We’ve reviewed the logs and diagnostics available to us and we believe the connectivity issue you’re experiencing may be the result of using clustering technology that assigns the frontend IP address to a loopback or virtual adapter (also known as a floating IP address). This is not a supported scenario on Azure. To correct your connectivity issue, we must assign the IP address to a physical network interface instead of a virtual adapter. Please take steps to correct this issue and let us know if you have any further questions.

Best regards,
<!--/issueDescription-->