<properties
    pageTitle="Security Policy - Policy Settings - Auto Provisioning Common Solutions"
    description="Security Policy - Policy Settings - Auto Provisioning Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636893"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="7c782d6f-50cd-4658-88e3-d89a210205f2"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Policy - Policy Settings - Auto Provisioning Common Solutions

To collect the data from the virtual machines install the **Microsoft Monitoring Agent**. Installation of the agent can be done automatically (recommended) or you can choose to install the agent manually.

     **Note:** Automatic provisioning is off by default. To set **Security Center** to install automatic provisioning by default, change the setting from off to on.

When automatic provisioning is set to **on**, **Security Center** provisions the **Microsoft Monitoring Agent** on all existing supported **Azure Virtual Machines (VMs)**, and any new ones that are created. Automatic provisioning is strongly recommended, but manual agent installation is also available. [Learn how to install the Microsoft Monitoring Agent extension](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#manualagent).

Windows or Linux IaaS VMs qualify for automatic provisioning of the **Microsoft Monitoring Agent** installation if the following conditions apply:

* The Microsoft Monitoring Agent extension is not currently installed on the VM
* The VM is in running state
* The Windows or Linux [Azure Virtual Machine Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows) is installed
* The VM is not used as an appliance such as web application firewall or next generation firewall

## **Recommended Documents**

* [Enable automatic provisioning of Microsoft Monitoring Agent](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#enable-automatic-provisioning-of-microsoft-monitoring-agent)<br>
* [Qualifications for VMs for Automatic Provisioning](https://docs.microsoft.com/azure/security-center/security-center-faq#what-qualifies-a-vm-for-automatic-provisioning-of-the-microsoft-monitoring-agent-installation)

## Troubleshooting

* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

## FAQ

* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
