<properties
	pageTitle="Domain Service is experiencing a network error"
	description="Azure AD Domain Services"
	infoBubbleText="See details on the right"
	service="microsoft.aad"
	resource="Microsoft_AAD_DomainServices"
	authors="jicha"
	displayOrder="1"
	articleId="DomainServices_NetworkAlert"
	diagnosticScenario="DomainServicesNetworkAlert"
	selfHelpType="diagnostics"
	supportTopicIds="Azure AD Domain Services"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Network Health Alert for Azure AD Domain Services

We are unable to reach the domain controllers for your managed domain due to network rules configured within your Azure virtual network.

Azure AD Domain Services requires access to specific ports in order to service and maintain your managed domain. To ensure that your managed domain works as expected, these ports must be open for access from Microsoft. To learn more about the networking requirements for managed domains please refer to this article:

[Ports required for Azure AD Domain Services](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-networking#ports-required-for-azure-ad-domain-services)

If we are unable to reach the domain controllers, your managed domain may be negatively affected, as Azure AD Domain Services will be unable to synchronize, and your users may have trouble signing-in. For help ensuring your network settings are configured to allow Microsoft to properly maintain your domain, please refer to the following article:

[Troubleshooting invalid networking configuration for your managed domain](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-troubleshoot-nsg#alert-aadds104-network-error)

#### Service Information

* Resource ID: **<!--$ResourceId-->ResourceId<!--/$ResourceId-->**
* Virtual Network experiencing network problems: **<!--$VirtualNetworkId-->VirtualNetworkId<!--/$VirtualNetworkId-->**
* Subnet domain services is enabled in: **<!--$SubnetName-->SubnetName<!--/$SubnetName-->**
* Virtual Machine experiencing network problems: **<!--$PrimaryVirtualMachineIp-->PrimaryVirtualMachineIp<!--/$PrimaryVirtualMachineIp-->, <!--$SecondaryVirtualMachineIp-->SecondaryVirtualMachineIp<!--/$SecondaryVirtualMachineIp-->**

#### Failed Network Diagnostics
Below are network diagnostics tests that have failed when we ran them on your managed domain. Each test included details a network rule that has been created that blocks service to the ports required for Azure AD Domain Services. These rules need to be modified for your managed domain to be synchronized. To learn more about resolving this alert, please visit https:/aka.ms/aadds-neterr

**<!--$NetworkTestResults-->NetworkTestResults<!--/$NetworkTestResults-->**
