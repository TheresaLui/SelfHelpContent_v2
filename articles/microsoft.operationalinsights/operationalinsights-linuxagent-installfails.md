
<properties
    pageTitle="Linux Agent/Installation fails"
    description="Installation of OMS Agent for Linux fails."
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="johnkemnetz"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612468"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Blackforest, Fairfax, usnat, ussec"
	articleId="2c537456-ed05-4843-8290-6a71eddc1825"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Linux Agent/Installation fails 

## **Recommended steps**
To resolve common installation failures, try one or more of the following methods:

* Review the [list of supported distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) and verify that you are installing on a supported machine. If you are trying to install on an unsupported distribution or version, or are using a custom VM image, [visit the OMS Linux agent Github repo](https://github.com/Microsoft/OMS-Agent-for-Linux) for guidance on forking the agent repo to create an agent that meets your needs.
* If you [receive a 403 error when installing the agent](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support#issue-you-receive-a-403-error-when-trying-to-onboard), run the `date` command on the Linux machine. If the date is over 15 minutes ahead or behind the current time, onboarding will fail. Also ensure that the workspace ID and workspace key you provided are correct and up to date.
* Review the [list of installation error codes](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#installation-error-codes) for common installation issues .
* Review the output of the installation script and check the [agent log files](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#important-log-locations-and-log-collector-tool) to identify any other errors.

## **Recommended documents**

[Supported Linux distros and versions](https://docs.microsoft.com/azure/virtual-machines/extensions/oms-linux#operating-system) <br>
[Common installation error codes](https://github.com/Microsoft/OMS-Agent-for-Linux/blob/master/docs/Troubleshooting.md#installation-error-codes) <br>
[Linux agent troubleshooting guide](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-linux-support)
