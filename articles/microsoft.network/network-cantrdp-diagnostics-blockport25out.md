<properties
pageTitle="BlockPort25Out"
description="BlockPort25Out"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_BlockPort25Out"
diagnosticScenario="BlockPort25Out"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue
<!--issueDescription-->
Starting on Nov. 15, 2017, all new PAYG/MPN subscriptions will have port 25 blocked for all deployments in the subscription. For Pay-As-You-Go or Microsoft Partner Network subscriptions created after November 15, 2017, there will be technical restrictions blocking e-mail sent directly from VMs in these subscriptions on TCP port 25.  Pay-As-You-Go or Microsoft Partner Network customers that need the ability to send e-mail from Azure VMs directly to external e-mail providers on port 25 (not using an authenticated SMTP relay) can make a request to remove the restriction.  Requests will be reviewed and approved at Microsoft’s discretion and will be only granted after additional anti-fraud checks are performed.
<!--/issueDescription-->

## **Recommended Documents**

 * [Azure Port 25 Update](https://blogs.msdn.microsoft.com/mast/2017/11/15/enhanced-azure-security-for-sending-emails-november-2017-update/)
