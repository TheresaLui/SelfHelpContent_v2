
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
cloudEnvironments="Public, Fairfax, usnat, ussec"
    articleId="1776cd2c-92b4-400e-9277-38ad60f8d03b"
    ownershipId="AzureMonitoring_LogAnalytics"
/>

# Questions about Update Compliance

## Ensuring devices are configured correctly to send data

The first step to troubleshooting is ensuring that devices are configured as documented on [Manually Configuring Devices for Update Compliance](https://docs.microsoft.com/windows/deployment/update/update-compliance-configuration-manual). We recommend using the [Update Compliance Configuration Script](https://docs.microsoft.com/windows/deployment/update/update-compliance-configuration-script) for troubleshooting and configuring devices.

### Devices have been correctly configured but aren't showing up in Update Compliance

It takes some time for data to appear in Update Compliance for the first time and if a Commercial ID has recently changed for a device. To learn more about data latencies for Update Compliance, refer to the official documentation covering [Update Compliance Data Latency](https://docs.microsoft.com/windows/deployment/update/update-compliance-using#update-compliance-data-latency).

## Devices are appearing, but without a device name or device name appearing as '#'

Device Name is now an opt-in via policy as of Windows 10, 1803. See the required policies for enabling device name at [Manually Configuring Devices for Update Compliance](https://docs.microsoft.com/windows/deployment/update/update-compliance-configuration-manual).

## Using Update Compliance with Desktop Analytics

Devices can be configured to send data to both Update Compliance and Desktop Analytics. In order to do this, you must ensure that Desktop Analytics and Update Compliance are using the same Log Analytics workspace. See the [Desktop Analytics FAQ](https://docs.microsoft.com/configmgr/desktop-analytics/faq) for more information.

## Windows Analytics retirement

As of January 31, 2020, Windows Analytics: Upgrade Readiness and Device Health solutions have been retired and data is no longer being provided to those solutions. Data will age out according to each customer's data retention policies. Customers can learn more about the retirement by referring to the [Windows Support article](https://support.microsoft.com/help/4521815/windows-analytics-retirement) addressing the retirement.

## **Recommended Documents**

* [Update Compliance official documentation](https://docs.microsoft.com/windows/deployment/update/update-compliance-monitor)
* [Desktop Analytics official documentation](https://docs.microsoft.com/configmgr/desktop-analytics/)
