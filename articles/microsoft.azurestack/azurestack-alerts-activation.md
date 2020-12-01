<properties
  pagetitle="Azure Stack Activation"
  service="microsoft.azurestack"
  resource="registrations"
  ms.author="alexsmit,justinha,patricka"
  selfhelptype="Generic"
  supporttopicids="32630572"
  resourcetags=""
  productpesids="16226,17058,17057,17322"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-alerts-activation"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack Activation

Windows products on Azure Stack must be used in accordance with Product Use Rights and Microsoft license terms.

## **Recommended Steps**

1. Azure Stack hosts activate all VMs that run Windows Server by using [Automatic Virtual Machine Activation (AVMA)](https://docs.microsoft.com/windows-server/get-started-19/vm-activation-19)
2. VMs that run Windows Server 2012 or earlier are not activated automatically, and must be activated by using <a href="https://docs.microsoft.com/previous-versions/tn-archive/ff793438(v=technet.10)">MAK activation</a>, with your own product key
3. If you move a Windows VM from Azure Stack to Azure and encounter activation problems, see [Troubleshoot Azure Windows virtual machine activation problems](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems)

## **Recommended Documents**

* [Troubleshoot Azure Windows virtual machine activation problems](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems)
* [Troubleshooting Windows activation failures on Azure VMs](https://blogs.msdn.microsoft.com/mast/2017/06/14/troubleshooting-windows-activation-failures-on-azure-vms/) for Windows Server 2012 R2 and newer versions<br>
* <a href="https://docs.microsoft.com/previous-versions/tn-archive/ff793438(v=technet.10)">MAK activation</a> for Windows Server 2012 and earlier versions