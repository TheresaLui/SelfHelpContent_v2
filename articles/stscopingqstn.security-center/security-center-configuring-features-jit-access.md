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

* The subscription Onboarded to Azure Defender (see [Pricing Page](https://azure.microsoft.com/pricing/details/security-center/) for more)
* The VM must be ARM deployed (classic VM is not supported)
* The VM must have an attached NIC:

  * The NIC has an NSG attached to it
  * The NIC is associated with a Subnet which has an NSG attached to it

* The VM’s OS must be Linux or Windows
* The VM is not already JIT configured (should not be already configured in a policy)
* Check the JIT discovery flow chart [here](https://docs.microsoft.com/azure/security-center/just-in-time-explained#how-security-center-identifies-which-vms-should-have-jit-applied)

### Access request can be initiated from these sources

- [From the portal](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-asc%2Cjit-request-asc#enable-jit-vm-access-) (Security Center -> Azure Defender -> Just-in-time VM access)
- [VM Connet](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-avm%2Cjit-request-asc#enable-jit-vm-access-)
- PowerShell
- [REST API](https://docs.microsoft.com/rest/api/securitycenter/jitnetworkaccesspolicies)  
* [Request access to a JIT-enabled VM](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-avm%2Cjit-request-asc#request-access-to-a-jit-enabled-vm)

### Request access RBAC Roles (permissions)

* Owner
* Contributor
* Security Admin
* Custom roles: For the least permissive JIT access request find out [what permissions are needed to configure and use jit](https://docs.microsoft.com/azure/security-center/just-in-time-explained#what-permissions-are-needed-to-configure-and-use-jit) to configure custom RBAC role

### NSG rules

* Upon JIT policy creation (configuring VM) a deny rule is created in the attached NSG
* Deny rules created per VM including all ports defined in the policy and the Destination is the VM's **internal IP address**
* The Deny rule is created at low priority, usually > 1000, carrying the following naming convention: *SecurityCenter-JITRule_-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx* 
* When requesting access, a higher priority rule, usually at 100-110, carrying this naming convention: *SecurityCenter-JITRule-xxxxxxx-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx* (same as Deny, without the "_")
* If the NSG contain other rules, JIT will create its rules as above while changing the existing rules priorities based on the above logic
* NSG rules that carry different name than the above, it's not a JIT created rule

### PowerShell

The Az.Security module provides four cmdlets that are relevant to Just in Time (JIT):

* [Get-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Get-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Remove-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Set-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Set-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Start-AzJitNetworkAccessPolicy](https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy?view=azps-4.7.0)
* [Enable JIT on your VMs using PowerShell](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-powershell%2Cjit-request-asc#using-just-in-time-vm-access-via-powershell)  
* [Request access to a JIT-enabled VM using PowerShell](https://docs.microsoft.com/azure/security-center/security-center-just-in-time?tabs=jit-config-powershell%2Cjit-request-powershell#request-access-to-a-jit-enabled-vm)  

### Activity Log

From JIT blade in the ASC portal you can right-click -> Activity Log to view the VMs access requests history. Look for 'Initiate JIT Network Access Policy' Activity Log to get access requests log.  

## Troubleshooting

### Can't connect after creating JIT access request

* Check for the VM NSG and make jure JIT allow request is created with highest priority. Verify:

  * Port – As requested
  * Protocol – TCP/UDP/Any
  * Source – IP address / CIDR / Any
  * Destination – Target VM private IP address**
  * Action – Allow
 
* If the VM is behind firewall, make sure adequate rule created for it as well
* Make sure you have the correct permissions to the VM access 
* Windows: Make sure the RDP file contain the correct IP address
* Linux: Make sure SSH port 22 accepting connection requests
* If no JIT rule exists, check the user permissions and the Activity Log for errors

**Note**: JIT rule destination is always the private IP address of the VM, even if you chose the public IP. This is the Azure Networking protocol called SNAT. More information about SNAL can be found [here](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections).

### JIT Connect (from VM Connect)

Just in Time (JIT) VM Connect is aimed to provide a fast and easy connection experience through the VM blade.

JIT Connect provides three parameters to configure: **IP Address**, **Port** and **Source IP**.  

* The time duration default as set in the policy
* Failing (error) while using the VM Connect JIT:
  * Try with different Source IP settings 
  * Make sure that the source IP is part of the VM's JIT policy allow range
* If you are behind proxy, choose "Other IP/IPs" and mark '*' for any
* For any other failure, try requesting using any other methods listed above

## **Recommended Documents**

* [Understanding just-in-time (JIT) VM access](https://docs.microsoft.com/azure/security-center/just-in-time-explained)
* [Secure your management ports with just-in-time access](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)
* [Automate JIT request with PowerShell](https://charbelnemnom.com/2018/10/version-2-automate-just-in-time-vm-access-request-with-powershell-azurerm-security-powershell/)
* Blog: [Why developers should enable JIT VM Access](https://azure.microsoft.com/blog/why-developers-should-enable-azure-security-center-s-just-in-time-vm-access/)
