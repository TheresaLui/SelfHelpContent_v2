<properties
	pageTitle="Check if the required ports are open for P2S VPN"
	description="Check if the required ports are open for P2S VPN"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="3afecd50-287d-4284-9035-7f6bcdc5c55a"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if the required ports are open for correct RADIUS connectivity

When the customer is using RADIUS authentication, there must be correct connectivity between the Gateway and the customer's RADIUS server.
  
It is a good test to use Test Traffic to check connectivity if the RADIUS server is on Azure:

## Recommended Steps

1. Check for NSGs or UDRs
   1. Identify the RADIUS server in ASC
   2. From the **Diagnostics** Tab, select **Test Traffic**
   3. Select "TunnelOrLocalIn" as the **Traffic Direction**
   4. Insert the DIP address of the Gateway instance as the **Source**
   5. Insert the IP address of the RADIUS as the **Destination**
   6. Populate UDP ports according to your scenario (by default 1812/1813)
   7. Execute the Test Traffic diagnostic by clicking on **Run**
2. Use the [Host-to-Guest Port Scanner Diagnostic](https://aka.ms/vmportscanner) to validate the VM running RADIUS is listening on required ports
   1. Verify the RADIUS server is in the virtual network (The RADIUS server must be in an Azure Virtual Network (either the one where the Gateway is, or another vnet connected to it). The RADIUS server can also be located on-premises, but only a VPN Site-to-Site connection can be used for connecting to a RADIUS server on-premises. An ExpressRoute connection cannot be used.)
   2. In ASC, go to Resource Explorer > Find the VM Running RADIUS > Select Diagnostics > port scanner
   3. Test ports 1812/1813 (Point to site using RADIUS authentication uses by default UDP ports 1812/1813. A custom RADIUS server implementation may use different ports)
