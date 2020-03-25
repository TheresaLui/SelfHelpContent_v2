
<properties
pageTitle="Questions about Windows Analytics"
description="Questions about Windows Analytics"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="jaimeo, zdvorak, mattreyn, chinglis"
ms.author="jaimeo, zdvorak, mattreyn, chinglis"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612530"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
	articleId="1776cd2c-92b4-400e-9277-38ad60f8d03b"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Questions about devices or names not appearing

**I've enrolled devices, but some of them aren't showing up in Upgrade Readiness**<br>

There is some latency in the system which means it could be a few days before all devices appear. But if you need to check sooner than that, try the steps in [Devices not appearing in Upgrade Readiness](https://docs.microsoft.com/windows/deployment/update/windows-analytics-faq-troubleshooting#devices-not-appearing-in-upgrade-readiness).

**I see devices in Upgrade Readiness or Update Compliance, but some of them aren't showing up in Device Health**

This could be a problem with the Commercial ID, the diagnostic data setting, or access to the necessary endpoints that collect the data. To diagnose and fix these problems, have a look at [Devices not appearing in Device Health Device Reliability](https://docs.microsoft.com/windows/deployment/update/windows-analytics-faq-troubleshooting#devices-not-appearing-in-device-health-device-reliability)



**How come I can see GUIDS for enrolled devices, but not their device names?**<br>

Starting with Windows 10, version 1803, you have to follow an extra step to allow the device names to be transmitted to Windows Analytics. To do this, change the value of the *AllowDeviceNameInTelemetry* by using Group Policy or Mobile Device Management. See the [Distributing policies at scale](https://docs.microsoft.com/windows/deployment/update/windows-analytics-get-started#deploying-windows-analytics-at-scale) section of the linked topic for more.  



## **Recommended Documents**

* [Enrolling devices in Windows Analytics](https://docs.microsoft.com/windows/deployment/update/windows-analytics-get-started)
* [Frequently asked questions and troubleshooting Windows Analytics](https://docs.microsoft.com/windows/deployment/update/windows-analytics-faq-troubleshooting)
* [Windows Analytics in the Azure Portal](https://docs.microsoft.com/windows/deployment/update/windows-analytics-azure-portal)
* [Windows Analytics and privacy](https://docs.microsoft.com/windows/deployment/update/windows-analytics-privacy)
