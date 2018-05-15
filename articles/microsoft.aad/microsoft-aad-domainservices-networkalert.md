<properties
	pageTitle="Domain Service is experiencing a network error"
	description="Network Issue Detected in Azure AD Domain Service"
	infoBubbleText="See details on the right"
	service="Microsoft.AAD"
	resource="DomainServices"
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

## Network Health Alert for Azure AD Domain Services

Hello [**Customer Name**],

We identified that your managed domain has an active Network Error alert. This means that Microsoft is unable to reach the domain controllers due to network rules you have set up on your domain.

Azure AD Domain Services requires access to specific ports in order to service and maintain your managed domain. In order to ensure your managed domain works as expected, these ports must be open for access from Microsoft. To learn more about the networking requirements, refer to this article:

[Ports required for Azure AD Domain Services](https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-networking#ports-required-for-azure-ad-domain-services)

While Microsoft is unable to reach the domain controllers, your managed domain may be negatively affected. We highly recommend you to edit your network settings to be compliant with our requirements. For steps to resolve the network error, refer to the following article:

[Troubleshooting invalid networking configuration for your managed domain](https://docs.microsoft.com/en-us/azure/active-directory-domain-services/active-directory-ds-troubleshoot-nsg#alert-aadds104-network-error)

#### Service Information
* Resource ID: <!--ResourceId-->[ResourceId]<!--/ResourceId-->
* Virtual Network experiencing network problems: <!--VirtualNetworkId-->[VirtualNetworkId]<!--/VirtualNetworkId-->
* Subnet domain services is enabled in: <!--SubnetName-->[SubnetName]<!--/SubnetName-->
* Virtual Machine experiencing network problems: <!--PrimaryVirtualMachineIp-->[PrimaryVirtualMachineIp]<!--/PrimaryVirtualMachineIp-->, <!--SecondaryVirtualMachineIp-->[SecondaryVirtualMachineIp]<!--/SecondaryVirtualMachineIp-->

#### Failed Network Diagnostics
Below are network diagnostics tests that have failed when we ran them on your managed domain. These may help you better troubleshoot which parts of your network are blocked:

<!--NetworkTestResults-->[NetworkTestResults]<!--/NetworkTestResults-->.

Please let us know if you have any questions or concerns.

Thank you,

[**Your Name**]
