<properties
  pagetitle="Unable to onboard a machine to Azure Arc for Servers by using the command `azcmagent connect`"
  service="microsoft.hybridcompute"
  resource="machines"
  ms.author="t-juwa"
  selfhelptype="Generic"
  supporttopicids="32689163,32689167,32689153,32689154,32689164,32689168"
  resourcetags=""
  productpesids="16872"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="482ad613-f6b9-45c6-a189-307ccfe560f0"
  ownershipid="Compute_HybridResourceProvider" />
# Unable to onboard a machine to Azure Arc for Servers by using the command `azcmagent connect`

This article will help with issues onboarding a machine to Azure Arc for Servers by using the command `azcmagent connect`.

## **Recommended Steps**

1. Your proxy configuration may be incorrect. [Update or remove proxy settings](https://docs.microsoft.com/azure/azure-arc/servers/manage-agent#update-or-remove-proxy-settings) shows the instructions to update your proxy settings. Arc for Servers does not support authenticated proxies, so make sure your proxy is unauthenticated. 
2. The Azcmagent client may not be able to reach our services in Azure. [Networking configuration](https://docs.microsoft.com/azure/azure-arc/servers/agent-overview#networking-configuration) shows the instructions to verify your Firewall/Gateway/Proxy settings to ensure the endpoints are whitelisted for access.
3. You may have provided an unsupported location as the Azure region. Run the following commands to get the list of locations for our resource provider, which will give you the display name for each region: 

  * CLI (Linux): `az provider show --namespace "Microsoft.HybridCompute" --query "resourceTypes[?resourceType=='machines'].locations | [0]"`
  * PowerShell (Windows): `$locations = Get-AzResourceProvider -ProviderNamespace Microsoft.HybridCompute | Where-Object { $_.ResourceTypes.ResourceTypeName -eq "machines" } | Select-Object -ExpandProperty Locations`

4. Find the ARM location name for the region’s display name: 

  * CLI (Linux):`az account list-locations --query "sort_by([].{DisplayName: displayName, ARMName:name}, &DisplayName)" --output table`
  * PowerShell (Windows): `Get-AzLocation | Where-Object DisplayName -in $locations | Select-Object Location`

5. If the above steps do not resolve your issue, please file a support ticket
