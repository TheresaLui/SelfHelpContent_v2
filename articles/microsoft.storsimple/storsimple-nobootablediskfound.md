<properties
	pageTitle="My virtual array isn't booting"
	description="My virtual array isn't booting"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My virtual array isn't booting.
If you can't boot the virtual array that was provisioned, verify the version of the virtual disk image that you are using. <br>
Common error messages: <br>
	1. `Boot failure. Reboot and Select proper Boot device`<br>
	2. `Insert Boot Media in selected Boot device`

## **Recommended steps**
* If using a VHD for Windows Server 2008 R2 or later, you will need to create a **Generation 1** VM.
* If using a VHDX for Windows Server 2012 or later, you will need to create a **Generation 2** VM.


## **Recommended documents**
[Provision a virtual array in Hyper-V.](https://aka.ms/storsimple-troubleshoot-provisionarray)<br>
[VHD for Hyper-V 2008 R2 and above](https://go.microsoft.com/fwLink/?LinkID=692085&clcid=0x409)<br>
[VHDX for Hyper-V 2012 and above](https://go.microsoft.com/fwLink/?LinkID=724278&clcid=0x409)<br>
[Generation 2 Virtual Machine Overview](https://technet.microsoft.com/library/dn282285.aspx)
