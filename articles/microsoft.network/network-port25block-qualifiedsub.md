<properties
pageTitle="Microsoft Azure has identified an issue with SMTP over TCP port 25"
description="Microsoft Azure has identified an issue with SMTP over TCP port 25"
infoBubbleText="Microsoft Azure has identified an issue. Please see details to the right."
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SmtpPort25BlockQualifiedSub"
diagnosticScenario="SmtpPort25BlockQualifiedSub"
selfHelpType="Diagnostics"
supportTopicIds="32592839, 32640601"
resourceTags="windows"
productPesIds="15526, 15660"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# This subscription is currently unauthorized to send mail over TCP port 25

<!--issueDescription-->
Your **'<!--$SubOfferType-->[SubscriptionOfferType]<!--/$SubOfferType-->'** subscription named **'<!--$SubscriptionName-->[SubscriptionName]<!--/$SubscriptionName-->'** is currently unauthorized to send mail from Azure VMs on TCP port 25. You may request to have this feature enabled for your subscription.
<!--/issueDescription-->

## **Recommended Steps**

Instead of using port 25, we strongly recommend using a secure SMTP relay as detailed [here](https://docs.microsoft.com/azure/virtual-network/troubleshoot-outbound-smtp-connectivity). VMs not utilizing an authenticated SMTP relay are frequently targeted by malicious users for their 'spam' operations. If you request to unblock port 25 for outbound traffic, you are acknowledging this risk and liability of fraud as agreed upon in the [Azure subscription agreement](https://azure.microsoft.com/support/legal/subscription-agreement/).
