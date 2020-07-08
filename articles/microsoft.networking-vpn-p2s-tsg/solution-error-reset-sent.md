<properties
	pageTitle="Error string Server did not respond properly to VPN control packets. Session state: Reset Sent"
	description="Error string Server did not respond properly to VPN control packets. Session state: Reset Sent"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="crcritel,stegag"
	ms.author="crcritel,stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="02f6d18b-dce5-4243-9d63-e6fff45f0546"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Solution for VPN Point-to-Site client Error string "Server did not respond properly to VPN control packets. Session state: Reset Sent"

The error *"Server did not respond properly to VPN control packets. Session state: Reset Sent"* is an Azure AD specific error. Follow the steps below to resolve configuration issues that cause this error.

## Recommended Steps

* The Shared Secret must be 512 HEX Chars. If it does not match the Server Shared Secret, then the connection would fail in the initial Open VPN Packet itself (Hard Reset Sent) since the HMAC validation in the packet would fail.
The customer can directly check the length of the Shared Secret in the **Azure VPN client** configuration page (Step 2 at this [link](https://docs.microsoft.com/en-us/azure/vpn-gateway/openvpn-azure-ad-client#connection) )

* The error is also seen when there are domain time synchronization issues on the client's clock. To fix this specific issue you need to run the following commands on the Client from CMD prompt with administrator privileges:
  * `w32tm /config /syncfromflags:domhier /update`
  * `net stop w32time`
  * `net start w32time`

## Recommended Documents

* https://docs.microsoft.com/en-us/azure/vpn-gateway/openvpn-azure-ad-client#connection
