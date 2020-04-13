<properties
    pageTitle="Can't connect after creating JIT access request"
    description="Issues connecting after creating a JIT access request"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680771"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="877a1428-9d6a-4c62-a4dc-e3ae861137b0"
	ownershipId="Azure_Security_Security_Center"
/>

# Can't connect after creating JIT access request

When initiating Just in Time (JIT) access request, a new network Security Group (NSG) Allow rule is created. This rule is removed when JIT defined duration exceeded.

### JIT naming conventions

JIT rules are carrying this naming convention, where the ‘x’ can be any number:

* SecurityCenter-JITRule-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Any other name belongs to rules that are not JIT-related.

### Check the JIT Allow rules

If your connection is still blocked after a JIT access request is initiated, check the existence of a JIT Allow rule under the virtual machine's (VMs) NSG and/or subnet NSG.

1. Click on the relevant Virtual Machine -> Networking:

2. Find the JIT Allow rule on the top
3. If a JIT rule exists, check that the following is specified:

    * Port – As requested
    * Protocol – TCP/UDP/Any
    * Source – IP address / CIDR / Any
    * Destination – Target VM private IP address**
    * Action – Allow

* If no JIT rule exists, check the user permissions and the Activity Log for errors
* If the source requesting access is behind a proxy, the option *My IP* may not work. You may need to define the full IP address range of the organization, or use "Source IP = Any (*)".

**Note**: JIT rule destination is always the private IP address of the VM, even if you chose the public IP. This is the Azure Networking protocol called SNAT. More information about SNAL can be found [here](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections).

## **Recommended Documents**

* [Manage virtual machine access using Just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)<br>
* [How to configure Just-in-time](https://docs.microsoft.com/azure/security-center/tutorial-protect-resources)
