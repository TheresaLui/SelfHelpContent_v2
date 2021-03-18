<properties
	  pageTitle="Port Scanner. Run port scanner from ASC"
	  description="Port Scanner. Run port scanner from ASC"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="f2346bb1-6f92-4e69-8610-e5b8942c3f25"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Port Scanner. Run port scanner from ASC

The port scan tool can be used to check the availability of a port on the OS level of a VM. This will help to identify if the Windows Firewall and OS application are configured correctly for the VM to receive the incoming traffic. 


## Recommended Steps

1. Navigate to the destination VM in ASC Resource Explorer
2.  Select the Diagnostics tab
3.  Select **Scan VM Ports**
4. Enter the destination ports to be scanned, separated by commas. Example: 40, 443, 3389.  You can use a hyphen to test a range. Example 20-22. (The destination IP address will be automatically entered.)
5. Run the test and review results


## Recommended Documents

1. [Port Scan TSG](https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/311342/ASC-Host-to-Guest-Port-Scanner-Diagnostic?anchor=using-the-host-to-guest-port-scanner)

