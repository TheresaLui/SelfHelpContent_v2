
<properties
    pageTitle="CloudServiceEndpointNotFound"
    description="CloudServiceEndpointNotFound"
    infoBubbleText="We have identified that your backup operation failed due network connectivity or service related issues"
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-cloudserviceendpointnotfound"
    diagnosticScenario="azurebackup-crc-cloudserviceendpointnotfound"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public"
/>


# Error CloudServiceEndpointNotFound


<!--issueDescription-->
We have identified that your backup operation failed due network connectivity or service related issues.
<!--/issueDescription-->


## **Recommended Steps**
To resolve this issue, perform the below:

- Retry the operation to resolve transient network issues. 
- Ensure the VM is connected to Internet and firewall, NSG, VPN or proxy server settings that are configured correctly to allow outbound communication with Azure Storage and Azure Backup endpoints as mentioned in this [article](https://aka.ms/AB-AA4dp5t).






