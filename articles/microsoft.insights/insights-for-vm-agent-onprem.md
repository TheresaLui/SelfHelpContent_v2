<properties
    pageTitle="I am having trouble installing the agent to my on-prem VM"
    description="I am having trouble installing the agent to my on-prem VM"
    infoBubbleText="Here are some things to help with installing our agent"
    service="microsoft.insights"
    resource="components"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-agent-onprem"
    productPesIds="17081"
    supportTopicIds="32738495"
    cloudEnvironments="public,fairfax, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

# I am having trouble installing the agent to my on-prem VM

If you have any problems installing the Log Analytics or Dependency agent as required for Azure Monitor for VMs, this information can help you. If you still can't resolve your problem, please contact Microsoft Support.



### Dependency agent installation problems:

**Installer prompts for a reboot**

The Dependency agent *generally* does not require a reboot after installation or removal. However, in certain rare cases, Windows Server requires a reboot to continue with the installation. This happens when a dependency, usually the Microsoft Visual C++ Redistributable library, requires a reboot because of a locked file.

**Message "Unable to install Dependency agent: Visual Studio Runtime libraries failed to install (code = [code_number])" appears**

The Microsoft Dependency agent is built on the Microsoft Visual Studio runtime libraries. You'll get a message if there's a problem during installation of the libraries.

The runtime library installers create logs in the %LOCALAPPDATA%\temp folder. The file is dd_vcredist_arch_yyyymmddhhmmss.log, where *arch* is x86 or amd64 and *yyyymmddhhmmss* is the date and time (24-hour clock) when the log was created. The log provides details about the problem that's preventing installation.

It might be useful to install the [latest runtime libraries](https://support.microsoft.com/help/2977003/the-latest-supported-visual-c-downloads) first.

The following  lists error codes and suggested resolution:

Error Code:  

 0x17 

Description:

 The library installer requires a Windows update that hasn't been installed. 
  
Resolution:

 Look in the most recent library installer log.<br><br>If a reference to Windows8.1-KB2999226-x64.msu is followed by a line Error 0x80240017: Failed to execute MSU package, you don't have the prerequisites to install KB2999226. Follow the instructions in the prerequisites section in [Universal C Runtime in Windows](https://support.microsoft.com/kb/2999226) article. You might need to run Windows Update and reboot multiple times in order to install the prerequisites.<br><br>Run the Microsoft Dependency agent installer again.



## **Recommended Documents**
### Log analytics agent installation problems

* [Windows agent troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows-troubleshoot)
* [Linux agent troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/agent-linux-troubleshoot)
* [VM extension troubleshooting](https://docs.microsoft.com/azure/azure-monitor/platform/vmext-troubleshoot)
