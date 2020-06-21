<properties
pageTitle="Microsoft Azure has information regarding SMTP over TCP port 25"
description="Microsoft Azure has information regarding SMTP over TCP port 25"
infoBubbleText="Microsoft Azure has information regarding SMTP over TCP port 25. Please see details to the right."
service="microsoft.network"
resource="virtualnetwork"
authors="anavinahar"
ms.author="anavin"
displayOrder=""
articleId="SmtpPort25AutoEnabledQualifiedSub"
diagnosticScenario="SmtpPort25BlockAlreadyEnabled"
selfHelpType="Diagnostics"
supportTopicIds="32592839, 32640601"
resourceTags="windows"
productPesIds="15526, 15660"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# This subscription has been evaluated and enabled to send mail over TCP port 25

<!--issueDescription-->
We found your Subscription **'<!--$SubscriptionName-->[SubscriptionName]<!--/$SubscriptionName-->'** of type **'<!--$SubOfferType-->[SubscriptionOfferType]<!--/$SubOfferType-->'** was disabled from sending emails on port 25. We have just evaluated your subscription and your subscription is **now enabled for all VMs to send mail on TCP port 25** per your request. Please stop/deallocate the VM/s from the portal, restart the VMs, and test again. 
<!--/issueDescription-->

If you continue to have issues sending mail from a VM's TCP port 25 in this subscription, you may be experiencing other routing related issues. We recommend the following steps to resolve the routing issue on your own.

## **Recommended Steps**

Try the following steps to resolve the issue:

1. Stop/Deallocate the VM from the portal, restart the VM, and test again. If your subscription was recently authorized to send mail on TCP port 25, stopping and starting the VM from the portal will cause the VM to pull the updated routing rules from the Azure platform.
2. Check your VM's network settings to determine if you have Network Security Groups (NSGs) blocking traffic. You can also use [Network Watcher's IP flow verify tool](https://docs.microsoft.com/azure/network-watcher/network-watcher-ip-flow-verify-overview) to check for NSGs blocking traffic, User-Defined Routes (UDRs) rerouting your traffic back to on-premises ('Default Route' 0.0.0.0/0), or to a network appliance.

If you still experience issues after trying the steps above, please provide the VM name and the TCP port you are attempting to send mail on for further diagnosis.

## **Recommended Documents**

* [Enhanced Azure Security for sending emails](https://docs.microsoft.com/azure/virtual-network/troubleshoot-outbound-smtp-connectivity)
