<properties
pageTitle="Microsoft Azure has identified an issue with SMTP over TCP port 25"
description="Microsoft Azure has identified an issue with SMTP over TCP port 25"
infoBubbleText="Microsoft Azure has identified an issue. Please see details to the right."
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SmtpPort25BlockUnQualifiedSub"
diagnosticScenario="SmtpPort25BlockUnQualifiedSub"
selfHelpType="Diagnostics"
supportTopicIds="32592839, 32640601"
resourceTags="windows"
productPesIds="15526, 15660"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>
# This subscription is unauthorized to send mail over TCP port 25
<!--issueDescription-->
We have found your subscription **'<!--$SubscriptionName-->[SubscriptionName]<!--/$SubscriptionName-->'**  of type **'<!--$SubOfferType-->[SubscriptionOfferType]<!--/$SubOfferType-->'**, without exception, **cannot be authorized** to send mail from Azure resources on TCP port 25.

Azure is committed to stopping SPAM and reducing the customer impact caused by negative IP reputation. Sending outbound email directly to external domains (such as outlook.com, gmail.com) from a virtual machine (VM) is available only for certain subscription types. Outbound SMTP connections using TCP port 25 (primarily used for unauthenticated email delivery) are blocked for most new subscriptions.
<!--/issueDescription-->

## **Recommended Steps**

* Please refer to the following article for more information on this restriction:
[Enhanced Azure security for sending emails](https://docs.microsoft.com/azure/virtual-network/troubleshoot-outbound-smtp-connectivity)
* If you have a requirement to send mail over TCP port 25, you can [create a new 'Pay-as-You-Go' subscription](https://azure.microsoft.com/pricing/purchase-options/) and submit a support request through that subscription for authorization to send mail on TCP port 25
