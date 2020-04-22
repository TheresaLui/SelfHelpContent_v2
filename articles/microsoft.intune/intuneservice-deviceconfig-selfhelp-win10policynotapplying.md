<properties
	pageTitle="I'm deploying a Windows 10 policy and it's not applying to the device."
	description="I'm deploying a Windows 10 policy and it's not applying to the device."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="deviceconfiguration_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="18b173a5-4b3a-44bc-a806-09bad3fb2018"
	ownershipId="IntuneCxP_Intune"
/>

# I'm deploying a Windows 10 policy and it's not applying to the device.

## **Recommended steps**

Follow one or more of these suggested steps help pinpoint why your Windows 10 policy isn't applying:
 
* Check to make sure that the policy is compatible with the Windows 10 version (such as 1709 and 1803) and product (such as Pro and Enterprise) that's on the device. For more information about specific policies and their supported Windows 10 products, see the [configuration service provider reference](https://docs.microsoft.com/windows/client-management/mdm/configuration-service-provider-reference).
* Go to [Troubleshoot](https://portal.azure.com/#blade/Microsoft_Intune_DeviceSettings/ExtensionLandingBlade/troubleshooting) to make sure the configuration profile is correctly assigned.
* Go to **Device configuration** to view the status of the deployment, and check for failures and errors. To learn how to collect logs and diagnose errors, view the [Intune documentation](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10).   

