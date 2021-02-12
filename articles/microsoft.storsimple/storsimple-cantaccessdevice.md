<properties
	pageTitle="I can’t access my device in File Explorer."
	description="I can’t access my device in File Explorer."
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="9000Or1200Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9313f8ab-00db-4b9c-ae55-5278f3c9c08a"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can’t access my device in File Explorer.
If you can't access your device in File Explorer, do the following.


## **Recommended steps**
1. In the local web UI of the virtual array, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**.
2. If accessing your device via the IP, check if you have used DHCP instead of a static IP. Your IP may have changed.
3. In the Azure portal for your StorSimple Device Manager, go to Devices blade and check if your device shows as deactivated.
4. Check the Hyper-V or ESX host for your VM to make sure that the VM is turned on and running.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[Troubleshooting Hyper-V](https://technet.microsoft.com/library/cc742454.aspx)<br>
[Troubleshooting VM failures on ESXi server](https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1003976)
