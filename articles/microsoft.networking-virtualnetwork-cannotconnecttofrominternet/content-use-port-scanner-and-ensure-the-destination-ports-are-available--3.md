<properties
	  pageTitle="Use port scanner and ensure the destination ports are available."
	  description="Use port scanner and ensure the destination ports are available."
      service="Microsoft.network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="00b17df1-2867-4287-ba9a-740a5ae92860"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Use port scanner and ensure the destination ports are available.

The port scan tool can be used to check the availability of a port on the OS level of a VM. This will help to identify if the windows firewall and OS application are configured correctly for the VM to receive the incoming traffic. 


## Recommended Steps

1. Navigate to the destination VM in ASC Resource Explorer
2. Select the **Diagnostics** Tab
3. Select the  **Scan VM Ports**
4. Enter destination ports to be scanned separated by commas. Example: 40, 443, 3389.  A dash can be used to test a range. Example 20-22. (The destination IP address will be automatically entered for you. )
5. Run test and review results


## Reccommended Documents

1.[Port Scan TSG](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/311342/ASC-Host-to-Guest-Port-Scanner-Diagnostic?anchor=using-the-host-to-guest-port-scanner)

