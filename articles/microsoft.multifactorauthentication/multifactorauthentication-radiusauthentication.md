<properties
	pageTitle="MFA Server (On-Premises)/Installing or configuring RADIUS authentication"
	description="MFA Server (On-Premises)/Installing or configuring RADIUS authentication"
	service="microsoft.multifactorauthentication"
	resource="Microsoft_AAD_IAM"
	authors="yossib"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32336331"
	resourceTags=""
	productPesIds="14947"
	cloudEnvironments="public"
/>

# Installing or configuring RADIUS authentication

## **Recommended steps**

1. Ensure that the RADIUS timeout configured on the VPN/application/device is sufficiently long to complete the MFA authentication. We generally recommend 60 seconds.
2. Ensure that the **shared secret** you entered on your RADIUS device matches the **shared secret** you entered in the MFA Server when you added the RADIUS client. 
3. Ensure that the **IP address** that you entered in the MFA Server when you added the RADIUS client is the IP that the requests are coming from. This step is especially important if there are multiple NICs/address on the device being secured. You should be able to determine this with a packet capture. The capture should also help you confirm that communication is occurring through the firewall. 

## **Recommended documents**

[Integrate RADIUS authentication with Azure Multi-Factor Authentication Server] (https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-radius)  
[Remote Desktop Gateway and Azure Multi-Factor Authentication Server using RADIUS] (https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-rdg)  
[Advanced scenarios with Azure Multi-Factor Authentication and third-party VPN solutions] (https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-advanced-vpn-configurations)  
[Integrate your existing NPS infrastructure with Azure Multi-Factor Authentication] (https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-extension)  
