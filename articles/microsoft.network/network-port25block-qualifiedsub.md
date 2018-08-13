<properties
pageTitle="Microsoft Azure has identified an issue with SMTP over TCP port 25"
description="Microsoft Azure has identified an issue with SMTP over TCP port 25"
infoBubbleText="Microsoft Azure has identified an issue. Please see details to the right."
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
displayOrder=""
articleId="SmtpPort25BlockQualifiedSub"
diagnosticScenario="SmtpPort25BlockQualifiedSub"
selfHelpType="Diagnostics"
supportTopicIds="32592839"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public"
/>
# This subscription is currently unauthorized to send mail over TCP port 25
<!--issueDescription-->
Your **'<!--$SubOfferType-->[SubscriptionOfferType]<!--/$SubOfferType-->'** subscription named **'<!--$SubscriptionName-->[SubscriptionName]<!--/$SubscriptionName-->'** is currently unauthorized to send mail from Azure VMs on TCP port 25. You may request to have this feature enabled for your subscription.

However, instead of using port 25, we strongly recommend using a secure SMTP relay as detailed [here](https://blogs.msdn.microsoft.com/mast/2017/11/15/enhanced-azure-security-for-sending-emails-november-2017-update/). VMs not utilizing an authenticated SMTP relay are frequently targeted by malicious users for their 'spam' operations. If you request to unblock port 25 for outbound traffic, you are acknowledging this risk and liability of fraud as agreed upon in the [Azure subscription agreement](https://azure.microsoft.com/support/legal/subscription-agreement/).
<!--/issueDescription-->

