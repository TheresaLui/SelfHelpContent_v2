<properties
	pageTitle="MFA Server (On-Premises)/Installing or configuring RADIUS authentication"
	description="MFA Server (On-Premises)/Installing or configuring RADIUS authentication"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="kgremban"
	displayOrder="250"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="mfa_overview"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e2b0749f-6c08-4a49-9389-98f394221161"
	ownershipId="AzureIdentity_User"
/>

# Troubleshoot RADIUS authentication configurations

## **Recommended steps**

1. Ensure that the RADIUS timeout configured on the VPN/application/device is sufficiently long to complete the MFA authentication. We generally recommend 60 seconds.
2. Ensure that the **shared secret** you entered on your RADIUS device matches the **shared secret** you entered in the MFA Server when you added the RADIUS client. 
3. Ensure that the **IP address** that you entered in the MFA Server when you added the RADIUS client is the IP that the requests are coming from. This step is especially important if there are multiple NICs/address on the device being secured. You should be able to determine this with a packet capture. The capture should also help you confirm that communication is occurring through the firewall. 

## **Recommended documents**

- [Integrate RADIUS authentication with Azure Multi-Factor Authentication Server](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-radius)  
- [Remote Desktop Gateway and Azure Multi-Factor Authentication Server using RADIUS](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-rdg)  
- [Advanced scenarios with Azure Multi-Factor Authentication and third-party VPN solutions](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-advanced-vpn-configurations)  
- [Integrate your existing NPS infrastructure with Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-nps-extension)  
