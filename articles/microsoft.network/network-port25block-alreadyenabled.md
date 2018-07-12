<properties
pageTitle="Microsoft Azure has information regarding SMTP over TCP port 25"
description="Microsoft Azure has information regarding SMTP over TCP port 25"
infoBubbleText="Microsoft Azure has information regarding SMTP over TCP port 25. Please see details to the right."
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
displayOrder=""
articleId="SmtpPort25BlockAlreadyEnabled"
diagnosticScenario="SmtpPort25BlockAlreadyEnabled"
selfHelpType="Diagnostics"
supportTopicIds="32592839"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public"
/>
#This subscription is authorized to send mail over TCP port 25
<!--issueDescription-->
We have found your Subscription **'<!--$SubscriptionName-->[SubscriptionName]<!--/$SubscriptionName-->'** of type **'<!--$SubOfferType-->[SubscriptionOfferType]<!--/$SubOfferType-->'** is **authorized** to send mail on TCP port 25. If you are having issues sending mail from a VM's TCP port 25 in this subscription, you may be experiencing other routing related issues. Please provide the VM name and the TCP port you are attempting to send mail on for further diagnosis. If you would like to resolve the routing issue on your own see the steps below.
##**Steps to resolve routing issues:**
Try the following two steps to resolve the issue: 
1. Stop/Deallocate the VM/s from the portal, start VM/s, test again. If your subscription was recently updated/enabled for the SMTP Port 25 feature, stopping & starting the VM/s from the portal will cause the VM to pull the updated routing rules from the Azure platform.
2. Check your VM's Network Setting blade to find if you have Network Security Groups (NSGs) blocking traffic or use [Network Watcher's IPflow verify tool](https://docs.microsoft.com/azure/network-watcher/network-watcher-ip-flow-verify-overview) to check for NSGs blocking traffic or User-Defined Routes (UDRs) rerouting your traffic back to on-premises ('Default Route' 0.0.0.0/0) or to a network appliance.

See [here](https://blogs.msdn.microsoft.com/mast/2017/11/15/enhanced-azure-security-for-sending-emails-november-2017-update/) for more information on this feature and why we are reporting this to you.
<!--/issueDescription-->
