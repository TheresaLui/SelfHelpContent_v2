<properties
    pageTitle="Azure Security Center – Configuring Features – Just-In-Time Access [JIT]"
    description="Azure Security Center – Configuring Features – Just-In-Time Access [JIT]"
    authors="v-miegge"
    ms.author="kawilson"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32693237"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="7e7f21c7-129d-4a7b-8b43-153b83880c7c"
	ownershipId="Azure_Security_Security_Center"
/>

# Azure Security Center – Configuring Features – Just-In-Time Access [JIT]

## JIT Access request failure

To request access for Just in Time (JIT), you need these permissions:

* Owner
* Contributor
* Security Admin
* Custom role:

  * For the least permissive access, a custom role can be defined to allow only JIT Access request, while denying any other involvement in the subscription
  * Custom roles definitions are described at [Manage virtual machine access using just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time#permissions-needed-to-configure-and-use-jit)

If you comply with all of the above, and still receive an error in the Activity Log, please continue creating the support request (providing the Activity Log JSON) and describe whether the request was initiated from the Security Center portal or from the virtual machine (VM) connect button.

## JIT API/Powershell issue

The Az.Security module provides three (3) cmdlets that are relevant to Just in Time (JIT):

* Get-AzJitNetworkAccessPolicy
* Set-AzJitNetworkAccessPolicy
* Start-AzJitNetworkAccessPolicy

For PowerShell usage and troubleshooting, please visit [Az.Security](https://docs.microsoft.com/powershell/module/az.security/).

## Can't connect after creating JIT access request

When initiating Just in Time (JIT) access request, a new network Security Group (NSG) Allow rule is created. This rule is removed when JIT defined duration exceeded.

### JIT naming conventions

JIT rules are carrying this naming convention, where the ‘x’ can be any number:

* **SecurityCenter-JITRule-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx**

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

**Note**: JIT rule destination is always the private IP address of the VM, even if you chose the public IP. This is the Azure Networking protocol called SNAT. More information about SNAT can be found at [Outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections).

## JIT Connect (from VM blade)

Just in Time (JIT) Connect is attached to the Azure Security Center JIT, and is aimed to provide a fast and easy connection experience through JIT.

JIT Connect provides two (2) parameters to configure: **IP Address** and **port**. The default is **Source IP = Any (*)**, and the time duration is set in the policy.

If you are unable to request access using JIT connect, try requesting using an ASC JIT Access request.

## JIT NSG Rules configuration

Just In Time (JIT) works through creating network Security Group (NSG) inbound rules. When first configured, JIT creates low priority **Deny** rules for each port that your JIT policy defines for the virtual machine (VM).

## JIT Policy issue

When a virtual machine (VM) is first configured to Just in Time (JIT), a policy is created defining the following parameters:

* PORT
* PROTOCOL
* ALLOWED SOURCE IPS
* IP RANGE
* TIME RANGE (HOURS)

After creating the policy, you can edit each one per VM from the **Security Center portal – Just in time VM** access blade.

### Using the Set-AzJitNetworkAccessPolicy PowerShell cmdlet

* When creating a new policy using PowerShell, the name must be set to "default"
* For any additional VMs that you want to add after first policy was set, you must create an array for all configured VMs. Otherwise, the current policy will override the existing "default" policy.

We are going to improve this behavior in the future.

## VM not recommended for JIT

The ASC recommendation *Just-In-Time network access control should be applied on virtual machines* lists all virtual machines (VMs) under the subscription, which do not have the JIT policy applied.

For a VM to be eligible for JIT:

* The subscription must be under Standard Pricing Tier. See [Pricing Page](https://azure.microsoft.com/pricing/details/security-center/) for more information.<br>
* The VM is deployed through ARM. Classic VMs are not supported
* NSG must exist on either VM or its subnet

## **Recommended Documents**

* [Manage virtual machine access using Just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)<br>
* [How to configure Just-in-time](https://docs.microsoft.com/azure/security-center/tutorial-protect-resources)
