<properties
pageTitle="Application Gateway 502 Error: Rule Ordering Insight"
description="Application Gateway 502 Error: Rule Ordering Insight"
infoBubbleText= "Issues with your Application Gateway were detected. See details on the right."
service="microsoft.network"
resource="applicationGateway"
authors="JRMayberry"
ms.author="rimayber"
displayOrder=""
articleId="83b5d001-18f7-4736-99d4-7f3cca8a42df"
diagnosticScenario=""
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec" 	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway 502 Error: Rule Ordering Insight

<!--issueDescription-->
Basic listener rule has a higher priority than the multi-site listener rule and points to an empty/unhealthy backend pool. Reorder the rules so that the rules with multi-site listener are at the top of the list and the basic listener rule is at the bottom with the lowest priority. You can do this by deleting the basic rule and recreating it again, so it goes to the bottom in the list.
<!--/issueDescription-->
