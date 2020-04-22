<properties
    pageTitle="VM not recommended for JIT"
    description="Details of eligible VMs for JIT"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680777"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="876aac56-7b42-45a9-96f2-e531ee1e66bc"
	ownershipId="Azure_Security_Security_Center"
/>

# VM not recommended for JIT

The ASC recommendation *Just-In-Time network access control should be applied on virtual machines* lists all virtual machines (VMs) under the subscription, which do not have the JIT policy applied.

For a VM to be eligible for JIT:

* The subscription must be under Standard Pricing Tier. See [Pricing Page](https://azure.microsoft.com/pricing/details/security-center/) for more information.<br>
* The VM is deployed through ARM. Classic VMs are not supported.
* NSG must exist on either VM or its subnet

## **Recommended Documents**

* [Manage virtual machine access using Just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)<br>
* [How to configure Just-in-time](https://docs.microsoft.com/azure/security-center/tutorial-protect-resources)
