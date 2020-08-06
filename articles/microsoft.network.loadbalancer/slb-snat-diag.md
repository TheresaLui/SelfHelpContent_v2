<properties
pageTitle="My VM is having outbound connectivity issues."
description="VM is having outbound connectivity issues due to SNAT exhaustion."
infoBubbleText="Issues with your VM outbound connections were detected. See details on the right."
service="microsoft.network"
resource="LoadBalancer"
authors="chadmath"
ms.author="chadmat"
displayOrder="1"
articleId="NetworkingSNATExhaustion"
diagnosticScenario="NetworkingSNATExhaustion"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,Fairfax,Mooncake, usnat, ussec"
ownershipId="CloudNet_LoadBalancer"
/>
# Source NAT (SNAT) Diagnostic Result

<!--issueDescription-->
Microsoft Azure has identified your virtual machine <!--$VirtualMachineName-->[VmName]<!--/$VirtualMachineName--> may be experiencing intermittent or unreliable connectivity with resources outside of Azure due to source NAT (SNAT) exhaustion.
<!--/issueDescription-->

## **Recommended Steps**

The Azure team has investigated and identified the source of your issue was source NAT (SNAT) port exhaustion on your VM's outbound connections. You can find a full explanation of this issue in detail [here](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#snatexhaust) along with several ways to mitigate. We apologize for any inconvenience this may have caused.

 
