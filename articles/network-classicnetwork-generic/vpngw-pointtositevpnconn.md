<properties
	pageTitle="Point to site VPN connectivity issues"
	description="Point to site VPN connectivity issues"
	service="microsoft.network"
	resource="virtualnetworkgateways"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32591156"
	resourceTags=""
	productPesIds="16094"
	cloudEnvironments="public"
/>

# Point to site VPN connectivity issues

## **Recommended steps**
If you are having problems connecting to your VPN from Windows 7 and Windows 8.1 such as VPN error 812 "The connection was prevented because of a policy configured on your RAS/VPN server" you may need to enable support for TLS 1.2. If that is the case, please follow the steps below:<br>
1.  Install the following updates:<br>
[KB3140245](https://www.catalog.update.microsoft.com/search.aspx?q=kb3140245)<br>
[KB2977292](https://www.microsoft.com/en-us/download/details.aspx?id=44342)<br>

2.  Open an admin command prompt by right-clicking on “Command Prompt” and selecting “Run as administrator”<br>

3.  Type and run the following commands from the admin command prompt:<br>
C:\> reg add HKLM\SYSTEM\CurrentControlSet\Services\RasMan\PPP\EAP\13 /v TlsVersion /t REG_DWORD /d 0xfc0<br>
C:\> reg add "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\WinHttp" /v DefaultSecureProtocols /t REG_DWORD /d 0xaa0<br>
C:\> if %PROCESSOR_ARCHITECTURE% EQU AMD64 reg add "HKLM\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Internet Settings\WinHttp" /v DefaultSecureProtocols /t REG_DWORD /d 0xaa0<br>
4.  Reboot the computer<br>
5.  Connect to the VPN<br>

## **Recommended documents**
Troubleshoot [point-to-site connection issues](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-troubleshoot-vpn-point-to-site-connection-problems)<br>
Check [point-to-site connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-vpn-faq#P2S) details<br>
Configure a [point-to-site VPN connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal)<br>
Generate and export [certificates for point-to-site connections](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-certificates-point-to-site) for Windows 10
