
<properties
pageTitle="Questions about Update Compliance"
description="Questions about Update Compliance"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="jaimeo, chinglis"
ms.author="jaimeo, chinglis"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612530"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
    articleId="1776cd2c-92b4-400e-9277-38ad60f8d03b"
    ownershipId="AzureMonitoring_LogAnalytics"
/>


# **Questions about Update Compliance**

## **Ensuring devices are configured correctly to send data**

The first step to troubleshooting is ensuring that devices are configured as documented on [aka.ms/uc-enrollment](https://aka.ms/uc-enrollment). We have a script to ensure this is the case, available at [aka.ms/uc-configuration-script](https://aka.ms/uc-configuration-script). Refer to the documentation for the script on how to use it for troubleshooting and configuring devices.

### **Devices have been correctly configured but aren't showing up in Update Compliance**

It takes some time for data to appear in Update Compliance for the first time and if a Commercial ID has recently changed for a device. To learn more about data latencies for Update Compliance, refer to [aka.ms/uc-data-latency](https://aka.ms/uc-data-latency).

## **Devices are appearing, but without a device name**

Starting with Windows 10, version 1803, you have to follow an extra step to allow the device names to be transmitted to Windows Analytics. To do this, change the value of the *AllowDeviceNameInTelemetry* by using Group Policy or Mobile Device Management. See the [Distributing policies at scale](https://docs.microsoft.com/windows/deployment/update/windows-analytics-get-started#deploying-windows-analytics-at-scale) section of the linked topic for more.  

## **Windows Defender Antivirus Reporting**

Update Compliance's reporting on Windows Defender Antivirus signature and threat status has been retired in favor of the [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager) offering which allows better monitoring capabilities.


## **Using Update Compliance with Desktop Analytics**

Devices can be configured to send data to both Update Compliance and Desktop Analytics. In order to do this, you must ensure that Desktop Analytics and Update Compliance are using the same Log Analytics workspace. See the [Desktop Analytics FAQ](https://docs.microsoft.com/configmgr/desktop-analytics/faq) for more information. 

## **Windows Analytics retirement**

As of January 31, 2020, Windows Analytics: Upgrade Readiness and Device Health solutions have been retired and data is no longer being provided to those solutions. Data will age out according to each customer's data retention policies. Customers can learn more about the retirement at [aka.ms/waretirement](https://aka.ms/waretirement). 


## **Recommended Documents**

* [Update Compliance official documentation](https://aka.ms/uc-docs)
* [Desktop Analytics official documentation](https://docs.microsoft.com/configmgr/desktop-analytics/)