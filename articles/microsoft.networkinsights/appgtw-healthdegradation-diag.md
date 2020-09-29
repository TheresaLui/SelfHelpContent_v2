<properties
pageTitle="The Application Gateway health has degraded status."
description="The Application Gateway health has degraded status."
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
ms.author="chadmat"
displayOrder="10"
articleId="AppGwHealthIsDegradedInsight"
diagnosticScenario="AppGwHealthIsDegradedInsight"
selfHelpType="Diagnostics"
supportTopicIds="32436961,32573483,32582834,32436964,32436960,32582828,32582829,32582830,32582825,32582826,32582827,32582831,32582832,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833"
resourceTags="windows"
productPesIds="15922"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Microsoft Azure has identified that your Application Gateway is in a degraded state

<!--issueDescription-->
We have identified that your Application Gateway **'<!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->' health is degraded** for metric '<!--$MetricName-->[MetricName]<!--/$MetricName-->'. This was most recently reported at <!--$PreciseTimeStamp-->[PreciseTimeStamp]<!--/$PreciseTimeStamp--> UTC.
<!--/issueDescription-->

## **Recommended Steps**

Consider stopping and starting the Application Gateway to recover impacted services via the following PowerShell commandlets: <br>

* `Stop-AzureRmApplicationGateway <!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->`
* `Start-AzureRmApplicationGateway <!--$Gatewayname-->[GatewayName]<!--/$Gatewayname-->`
