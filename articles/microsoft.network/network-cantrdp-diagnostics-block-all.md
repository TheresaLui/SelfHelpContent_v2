<properties
pageTitle="BlockAll"
description="BlockAll"
infoBubbleText="BlockAll"
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_BlockAll"
diagnosticScenario="BlockAll"
selfHelpType="diagnostic"
supportTopicIds=
resourceTags="windows"
productPesIds=
cloudEnvironments="public"
/>
# Connectivity Diagnostics Result
<!--issueDescription-->
Microsoft Azure has identified <!--$StatelfulAction-->[StatelfulAction]<!--/$StatelfulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because there is no security rule defined to allow this traffic. By default, security groups block all traffic when there is no security rule matching the traffic. If the access control (security rules) result is not desired, view the Effective Security Rules to determine if the addition or modification of a customer-defined security rule is required.
1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account.
2. Click Browse > Network Interface.
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network.
 <br>
<!--/issueDescription-->
