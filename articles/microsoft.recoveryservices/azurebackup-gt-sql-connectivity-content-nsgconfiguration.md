<properties
	  pageTitle="Check the NSG configuration of the VM"
	  description="Check the NSG configuration of the VM"
      service="Microsoft.RecoveryServices"
      resource="Microsoft.RecoveryServices/vaults"
	  authors="chgonugu"
	  ms.author="chgonugu"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="6fb9ceee-a697-425e-9c90-9b329550083f"
	  ownershipId="StorageMediaEdge_Backup"
/>

# Check the NSG configuration of the VM

Run below PowerShell cmdlets to white-list Azure Backup, Storage, Active Directory services for outbound network access.

## Add Azure account credentials
Add-AzureRmAccount
## Select the NSG subscription
Select-AzureRmSubscription "SubscriptionId"
## Select the NSG
$nsg = Get-AzureRmNetworkSecurityGroup -Name "<NSG name>" -ResourceGroupName "<NSG resource group name>"
## Add allow outbound rule for Azure Backup service tag
Add-AzureRmNetworkSecurityRuleConfig -NetworkSecurityGroup $nsg -Name "AzureBackupAllowOutbound" -Access Allow -Protocol * -Direction Outbound -Priority <priority> -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix "AzureBackup" -DestinationPortRange 443 -Description "Allow outbound traffic to Azure Backup service"
## Add allow outbound rule for Storage service tag
Add-AzureRmNetworkSecurityRuleConfig -NetworkSecurityGroup $nsg -Name "StorageAllowOutbound" -Access Allow -Protocol * -Direction Outbound -Priority <priority> -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix "Storage" -DestinationPortRange 443 -Description "Allow outbound traffic to Azure Backup service"
## Add allow outbound rule for AzureActiveDirectory service tag
Add-AzureRmNetworkSecurityRuleConfig -NetworkSecurityGroup $nsg -Name "AzureActiveDirectoryAllowOutbound" -Access Allow -Protocol * -Direction Outbound -Priority <priority> -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix "AzureActiveDirectory" -DestinationPortRange 443 -Description "Allow outbound traffic to AzureActiveDirectory service"
## Save the NSG
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup $nsg

