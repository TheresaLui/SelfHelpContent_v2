<properties
	  pageTitle="Perform a Get/Set of the Resource"
	  description="Perform a Get/Set of the Resource"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualWANs"
	  authors="stegag"
	  ms.author="stegag"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="7d0a7e59-61f7-47f5-9f66-343678f93766"
	  ownershipId="CloudNet_VirtualWAN"
/>

# Perform a Get/Set of the Resource

If a resource is in **Failed** provisioning state, it means that some previous operation on it failed for any reason.
Provisioning state is just a metadata property on the NRP resource. **Being in failed state doesn't impact the functionality of the resource**.

Customers may not notice or don't remember how the resource got into failed state. Also, it is possible that the original issue that caused the issue has disappeared since the original operation, but the failed state won't be automatically restored to succeeded. **Running a PUT operation is required to restore the provisioning state.**

For these reasons most of the times running a simple PUT operation will fix the issue without applying any change. Usually the best way to do this for most NRP objects is to **run a GET operation from powershell, and re-run a SET operation on it** (without changes). 

However the SET commands are sometimes missing for Virtual WAN related objects, for which the UPDATE command exists. It is discouraged to use Resource Explorer to achieve this, especially for Virtual WAN related resources.

These are some sample commands to restore Succeeded provisioning state on VirtualWan related objects:

Virtual WAN
```powershell
$virtualwan = Get-AzVirtualWan -ResourceGroupName RGName -Name VirtualwanName
Update-AzVirtualWan -InputObject $virtualwan
```

Virtual Hub
```powershell
$virtualhub = Get-AzVirtualHub -ResourceGroupName RGName -Name VirtualHubName
Update-AzVirtualHub -InputObject $virtualhub
```

VpnSite
```powershell
$vpnsite = Get-AzVpnSite -ResourceGroupName RGName -Name vpnsitename 
Update-AzVpnSite -InputObject $vpnsite
```

Hub Route Table
```powershell
$routetable = Get-AzVHubRouteTable -ResourceGroupName RGName -HubName VirtualHubName -Name TableName
Update-AzVHubRouteTable -InputObject $routetable
```
Note: this doesn't apply for the "Default" route table. if the Default route table is in failed state, the only way to generate a PUT operation on it is to add a dummy route to it.

VpnGateway
```powershell
$vpngateway = Get-AzVpnGateway -ResourceGroupName RGName -Name 9b9b993d403243fa8c181cda2668666e-westeurope-gw
Update-AzVpnGateway -InputObject $vpngateway
```
P2sGateway
```powershell
$p2sgateway = Get-AzP2sVpnGateway -ResourceGroupName RGName -Name 49e0c9ffda794fa1b1178a7bf8ffc5ed-westeurope-p2s-gw
Update-AzP2sVpnGateway -InputObject $p2sgateway
```

Azure Firewall (for Secure Hubs)
```powershell
$firewall = Get-AzFirewall -Name AzureFirewall_securehub -ResourceGroupName securewan
Set-AzFirewall -AzureFirewall $firewall
```

Please identify the correct command from the list based on the object type, and ask customer to run it.

If running the command doesn't fix the provisioning state, it means that the underlying issue is still outstanding.
In this case, the next step is to identify the PUT you have just performed, and troubleshoot it.
