<properties
pageTitle="Probe Host And Backend FQDN Mismatch"
description="Probe Host And Backend FQDN Mismatch"
infoBubbleText="Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="ApplicationGateway"
authors="chadmath"
displayOrder="10"
articleId="probehostandbackendfqdnmismatch"
diagnosticScenario="probehostandbackendfqdnmismatch"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Application Gateway Health Probe FQDN Mismatch
<!--issueDescription-->
We have identified that the Host listed for Health Probe **<!--$ProbeHost-->[ProbeHost]<!--/$ProbeHost-->** does not match the FQDN for the Backend pool resources. With this mismatch the health probe from the Application Gateway will not reach the backend pool resources which will remove the backend pool resrouces to be removed from load-balanced rotation breaking your solution.
<!--/issueDescription-->
## **Steps to resolve the issue**

1. Go to the 'backend pools' blade and select the backend pool you want for Health Probe **<!--$ProbeHost-->[ProbeHost]<!--/$ProbeHost-->**.
2. Make note of the FQDN used and close the blade.
3. Go to the 'Health Probes' blade and select **<!--$ProbeHost-->[ProbeHost]<!--/$ProbeHost-->**.
4. Update the 'Host' field with the FQDN from step #2 above.
