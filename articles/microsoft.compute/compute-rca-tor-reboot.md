<properties
pageTitle="ComputeRcaTorReboot"
description="ComputeRcaTorReboot"
infoBubbleText="Issues with your resource were detected. See details on the right."
service="microsoft.compute"
resource="VirtualMachine"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="ComputeRcaTorReboot"
diagnosticScenario="ComputeRcaTorReboot"
selfHelpType="RCA"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>
# Root Cause Analysis Summary:
<!--issueDescription-->
The Azure team has investigated and identified the source of your issue was maintenance of the network switch which connects the physical node running your VM.  Maintenance is performed to ensure the long term reliability, security, and integrity of the Azure platform.  We apologize for any inconvenience this may have caused. 
<!--/issueDescription-->
[Learn more](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) on ways to set up and manage multiple virtual machines to ensure high availability for your VM applications through maintenance and downtime events.
 <br>
