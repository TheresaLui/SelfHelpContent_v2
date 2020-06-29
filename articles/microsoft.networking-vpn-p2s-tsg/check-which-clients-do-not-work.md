<properties
	pageTitle="Check which clients don't work"
	description="Check which clients don't work"
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
	articleId="1f38b447-abe3-4d29-aa5d-3302ae3ccc97"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check which clients don't work

Discuss with the customer and try to gather as much detail as possible on what kind of clients are failing.
The aim is to identify what is common between the failing clients (the OS? protocol?) and what is different between the working clients and failing ones.

## Recommended Steps

1. Determine the VPN client protocol
   1. Go to ASC > Resource Explorer and select the VPN gateway. <br/>
   2. Check the **VPN Tunneling Protocols** property and identify if more than one protocol has been enabled. <br/>
   3. If so, ask the customer if the clients failing and those working connect using different protocols?
2. Determine the Authentication method**
   1. Go to ASC > Resource Explorer and select the VPN gateway.
   2. Identify the CustomerSubscriptionID, ResourceID and Region
   3. From Jarvis Actions open [Get NRP Subscription details](https://jarvis-west.dc.ad.msft.net/?page=actions&acisEndpoint=Public&managementOpen=false&published=true&selectedNodeType=3&extension=NRP&group=NRP%20Subscription%20Operations&operationId=GetNrpSubscriptionDetails&operationName=Get%20NRP%20Subscription%20Details&inputMode=single&actionEndpoint=Production&genevatraceguid=2f5b46cb-30d3-401a-84c5-68adbfecd5ee)
   4. Run the command by providing the CustomerSubscriptionID and Region as parameters
   5. From the command output, locate the VPN gateway by searching for the ResourceID
   6. If a "vpnClientRootCertificates" parameter exists and is not empty -> the authentication method is **Certificates**
   * If a "RadiusServerAddress" parameter exists and is not empty -> the authentication method is **RADIUS** <br/>
   * If an "aadTenant" parameter exists and is not empty -> the authentication method is **Azure AD**
3. Determine the Client OS**
   1. Ask the customer if the clients failing and those working are running different OSes?
4. Based on the information gathered in logs and that received from customer, try to determine if the subset of non-working clients is in a supported scenario. The following tables summarizes the supportability for client OS vs protocols and authentication method.

**For Certificates or RADIUS authentication** <br>
**| Client OS | Protocol | Client| Supported?  <br>**
| Windows   | SSTP or IKEv2 | Native Windows Client | YES <br>
| Windows   | OpenVPN       | Native Windows Client | NO <br>
| Windows   | SSTP or IKEv2 |Azure VPN Client | NO <br>
| Windows   | OpenVPN       | Azure VPN Client | YES <br>
| Windows   | SSTP or IKEv2 | OpenVPN client | NO <br>
| Windows   | OpenVPN| OpenVPN client | YES <br>
| Mac OS | SSTP or OpenVPN | Native Mac Client | NO <br>
| Mac OS | IkeV2| Native Mac Client | YES <br>
| Mac OS | SSTP or IKEv2 | OpenVPN client | NO <br>
| Mac OS | OpenVPN| OpenVPN client | YES <br>
| Linux | SSTP or OpenVPN | Strongswan | NO <br>
| Linux | IkeV2| Strongswan | YES <br>
| Linux | SSTP or IKEv2| OpenVPN client | NO <br>
| Linux | OpenVPN| OpenVPN client | YES <br>
| Other OS | SSTP or IKEv2 | any | NO <br>
| Other OS | OpenVPN| OpenVPN client | YES <br>

***Note***: any other combination not covered in the table is NOT supported.

**For Azure AD authentication** <br>
**| Client OS | Protocol | Client| Supported?**   <br>
| Windows | any| Native Windows Client | NO <br>
| Windows | any| OpenVPN client | NO <br> 
| Windows | SSTP or IKEv2 |Azure VPN Client | NO <br>
| **Windows** | **OpenVPN**| **Azure VPN Client** | **YES** <br>
| Mac OS | any| any | NO <br>
| Linux | any| any| NO <br>
| Other OS | any | any | NO <br>

***Note***: any other combination not covered in the table is NOT supported.
