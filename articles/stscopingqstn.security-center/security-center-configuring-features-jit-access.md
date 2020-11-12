<properties
  pagetitle="Just-in-time VM access (JIT) self-help guide"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32693237"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="7e7f21c7-129d-4a7b-8b43-153b83880c7c"
  ownershipid="Azure_Security_Security_Center" />
# Just-in-time VM access (JIT) self-help guide

### Conditions for a VM to be recommended (for JIT configuration)

* The subscription is onboarded to Azure Defender (for more information, see [Pricing](https://azure.microsoft.com/pricing/details/security-center/))
* The VM must be ARM deployed (classic VM is not supported)
* The VM must have an attached NIC:
  * The NIC has an NSG attached to it
  * The NIC is associated with a subnet that has an NSG attached to it

* The VM’s OS must be Linux or Windows
* The VM is not already JIT configured (should not be already configured in a policy)
* Check the [JIT discovery flow chart](https://docs.microsoft.com/azure/security-center/just-in-time-explained#how-security-center-identifies-which-vms-should-have-jit-applied)

### Access request can be initiated from these sources

- [From Azure Portal](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-asc%2Cjit-request-asc#enable-jit-vm-access-) (Security Center > Azure Defender > Just-in-time VM access)
- [VM Connect](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-avm%2Cjit-request-asc#enable-jit-vm-access-)
- PowerShell
- [REST API](https://docs.microsoft.com/rest/api/securitycenter/jitnetworkaccesspolicies)  
* [Request access to a JIT-enabled VM](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-avm%2Cjit-request-asc#request-access-to-a-jit-enabled-vm)

### Request access RBAC Roles (permissions)

* Owner
* Contributor
* Security Admin
* Custom roles: For the least permissive JIT access request, see [what permissions are needed to configure and use jit](https://docs.microsoft.com/azure/security-center/just-in-time-explained#what-permissions-are-needed-to-configure-and-use-jit) to configure a custom RBAC role

### NSG rules

* On JIT policy creation (configuring VM), a deny rule is created in the attached NSG
* Deny rules are created per VM, including all ports defined in the policy, and the destination is the VM's **internal IP address**
* The Deny rule is created at a low priority, usually > 1000, with the following naming convention: *SecurityCenter-JITRule_-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx* 
* When requesting access, this is a higher priority rule, usually at 100-110, with the following naming convention: *SecurityCenter-JITRule-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx* (same as Deny, without the "_")
* If the NSG contains other rules, JIT will create its rules, while changing the existing rules' priorities, based on the logic above
* If an NSG rule has a name different then the names specified above, it's not a JIT created rule

### PowerShell

The Az.Security module provides four cmdlets that are relevant to Just in Time (JIT):

* [Get-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Get-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Remove-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Set-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Set-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Start-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Enable JIT on your VMs using PowerShell](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-powershell%2Cjit-request-asc#using-just-in-time-vm-access-via-powershell)  
* [Request access to a JIT-enabled VM using PowerShell](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-powershell%2Cjit-request-powershell#request-access-to-a-jit-enabled-vm)  

### Activity Log

From the JIT blade in the ASC portal, right-click **Activity Log** to view the VMs access requests history. Look for the **Initiate JIT Network Access Policy** Activity Log to get the access requests log.  

## Troubleshooting

### Can't connect after creating JIT access request

* Check for the VM NSG and make sure that the JIT allow request is created with highest priority. 
  Verify the following:

  * Port – As requested
  * Protocol – TCP/UDP/Any
  * Source – IP address / CIDR / Any
  * Destination – Target VM private IP address (see the following Note)
  * Action – Allow
 
* If the VM is behind the firewall, make sure an adequate rule created for it, as well
* Make sure you have the correct permissions to the VM access 
* Windows: Make sure the RDP file contains the correct IP address
* Linux: Make sure that SSH port 22 is accepting connection requests
* If no JIT rule exists, check the user permissions and the Activity Log for errors

**Note**: The JIT rule destination is always the private IP address of the VM, even if you chose the public IP. This is the Azure Networking protocol called SNAT. [Learn more about SNAT](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections).

### JIT Connect (from VM Connect)

Just in Time (JIT) VM Connect provides a fast, easy connection experience through the VM blade.

JIT Connect provides three parameters to configure: **IP Address**, **Port**, and **Source IP**.  

* The time duration default as set in the policy
* Failing (error) while using the VM Connect JIT:
  * Try with different Source IP settings 
  * Make sure that the source IP is part of the VM's JIT policy allow range
* If you are behind the proxy, choose **Other IP/IPs** and mark ***** for any
* For any other failure, try requesting using any other methods listed above

## **Recommended Documents**

* [Understanding just-in-time (JIT) VM access](https://docs.microsoft.com/azure/security-center/just-in-time-explained)
* [Secure your management ports with just-in-time access](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)
* Blog: [Why developers should enable JIT VM Access](https://azure.microsoft.com/blog/why-developers-should-enable-azure-security-center-s-just-in-time-vm-access/)
