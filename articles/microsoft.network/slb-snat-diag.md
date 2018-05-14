<properties
pageTitle="My VM is having outbound connectivity issues."
description="VM is having outbound connectivity issues due to SNAT exhaustion."
infoBubbleText="Issues with your VM outbound connections were detected. See details on the right."
service="microsoft.network"
resource="Software Load Balancer"
authors="chadmath"
displayOrder=""
articleId="SlbSnatExhaustionDiag"
diagnosticScenario="SlbSnatExhaustionDiag"
selfHelpType="resource"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Source NAT (SNAT) Diagnostic Result
<!--issueDescription-->
Microsoft Azure has identified your virtual machine <!--$VirtualMachineName-->[VMName]<!--/$VirtualMachineName--> may be experiencing intermittent or unreliable connectivity with resources outside of Azure due to source NAT (SNAT) exhaustion as described [here](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections).
 <br>
<!--/issueDescription-->
## Verification and Mitigation
Verify that customer observed impact was at the same time as the SNAT exhaustion time and has recovered via the 'troubleshooting' section of the [CSSWiki Workflow](https://www.csssupportwiki.com/index.php/curated:Troubleshooting_SNAT_Failures_(Outbound)) and [NetVMA]() for more details. Once verfied, send the customer the Customer Ready Content below.

## Customer Ready Content
The Azure team has investigated and identified the source of your issue was source NAT (SNAT) port exhaustion on your VM's outbound connections. You can find a full explanation of this issue in detail [here](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#snatexhaust) along with several ways to mitigate. We apologize for any inconvenience this may have caused. 

