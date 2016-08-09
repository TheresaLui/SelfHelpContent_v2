<properties
	pageTitle="My virtual array has turned off"
	description="My virtual array has turned off"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My virtual array has turned off.
This could be due to one of the following reasons:

## **Recommended steps**
1. The host on which the virtual array is provisioned has run out of disk space. If running Hyper-V, create additional space by doing the following:<br>
	1. Launch Hyper-V Manager. Go to Tools > Server Manager > Hyper-V Manager.<br>
	2. From the Virtual Machines list, identify the virtual array(s) in a  Paused-Critical state.<br>
	3. Free up resources so that the virtual array(s) can be booted. For example, you can free up the disk space on corresponding hard drives.<br>
	4. Right-click each virtual array, then click Resume. This returns the virtual machine to a running state.<br>
2. If the virtual array(s) has not run out of disk space, then try to turn it on.


## **Recommended documents**
[Troubleshoot via the local web UI](https://aka.ms/storsimple-troubleshoot-diagnostics)<br>
[Troubleshooting Hyper-V](https://technet.microsoft.com/en-us/library/cc742454.aspx)
