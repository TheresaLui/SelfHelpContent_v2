<properties
    pageTitle="JIT NSG Rules configuration"
    description="Configuring NSG rules with JIT"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680775"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="9f9225aa-b288-49fb-90e3-f43386d368d9"
	ownershipId="Azure_Security_Security_Center"
/>

# JIT NSG Rules configuration

Just In Time (JIT) works through creating network Security Group (NSG) inbound rules. When first configured, JIT creates low priority **Deny** rules for each port that your JIT policy defines for the virtual machine (VM).

### JIT naming conventions

The naming convention for the rule is:

* **SecurityCenter-JITRule-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx**

Any other naming convention is not created by JIT.

## **Recommended Documents**

* [Manage virtual machine access using Just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)<br>
* [How to configure Just-in-time](https://docs.microsoft.com/azure/security-center/tutorial-protect-resources)
