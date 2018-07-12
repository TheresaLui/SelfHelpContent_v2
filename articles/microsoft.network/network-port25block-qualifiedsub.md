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
#This subscription is currently unauthorized to send mail over TCP port 25
<!--issueDescription-->
Your subscription **'<!--$SubscriptionName-->[SubscriptionName]<!--/$SubscriptionName-->'**, of type **'<!--$SubOfferType-->[SubscriptionOfferType]<!--/$SubOfferType-->'**, is currently unauthorized to send mail from Azure VMs on TCP port 25, however, you may request to have this feature enabled for your subscription by continuing with support case creation in the Azure portal for this subscription.
<!--/issueDescription-->
##More Information
We recommend using an SMTP relay as detailed [here](https://blogs.msdn.microsoft.com/mast/2017/11/15/enhanced-azure-security-for-sending-emails-november-2017-update/). **WARNING**: VMs not utilizing an authenticated SMTP relay are frequently targeted by fraudulent actors to setup their operations. By continuing with this support request to unblock port 25 outbound you are acknowledging this risk and liability of fraud which was agreed to in your [Azure subscription agreement](https://azure.microsoft.com/support/legal/subscription-agreement/).
