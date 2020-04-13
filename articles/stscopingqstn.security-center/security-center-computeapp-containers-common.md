<properties
    pageTitle="Containers Common Solutions"
    description="Containers Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636869"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15r058d-1fg6-6b97-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Containers Common Solutions

Azure Security Center improves the security landscape by assessing your Docker container on your virtual machines in Azure.

**Azure Security Center Capabilities**

Azure Security Center now provides you with several new capabilities to help you secure your containers.

1. Visibility to the containers hosted on IaaS Linux machines:

    In Azure Security Center, a new tab of containers is now available and displays all virtual machines with Docker. When exploring the security issues of a virtual machine, Security Center now provides additional information related to the containers on the machine, such as Docker version and the number of images running on the host.

1. Security recommendations based on the CIS benchmark for Docker

    Security Center scans your Docker configurations and gives you visibility into misconfigurations by providing a list of all failed rules that were assessed. Security Center gives you guidelines to help you resolve these issues quickly and save time. Security Center continuously assesses the Docker configurations and provides you with their latest state.

1. Real time container threat detection

     Security Center now provides real-time threat detection for your containers on Linux machines with AuditD component.

     The alerts identify several suspicious Docker activities, such as the creation of a privileged container on host, an indication of Secure Shell (SSH) server run inside a Docker container, or the usage of crypto miners. You can use this information to quickly remediate security issues and improve the security of your containers.

## **Recommended Documents**

- [Understand Azure Security Center container recommendations](https://docs.microsoft.com/azure/security-center/security-center-container-recommendations)
- [Protect Linux containers running in IaaS with Azure Security Center](https://azure.microsoft.com/blog/protect-linux-containers-running-in-iaas-with-azure-security-center/)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)