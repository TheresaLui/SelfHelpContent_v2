<properties
    pageTitle="Azure Stack VM Activation"
    description="Azure Stack Windows Activation issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32630572"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-alerts-activation"
/>

# Azure Stack Activation

Windows products on Azure Stack must be used in accordance with Product Use Rights and Microsoft license terms.

## **Recommended Steps**

1. Azure Stack hosts activate all VMs that run Windows Server 2012 R2 or later using [Automatic Virtual Machine Activation (AVMA)](https://docs.microsoft.com/windows-server/get-started-19/vm-activation-19)
2. VMs that run Windows Server 2012 or earlier are not automatically activated and must be activated by using [MAK activation](https://docs.microsoft.com/previous-versions/tn-archive/ff793438(v=technet.10)), using your own product key.
3. If you move a Windows VM from Azure Stack to Azure and encounter activate problems, see [Troubleshoot Azure Windows virtual machine activation problems](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems).

## **Recommended Documents**

* [Troubleshoot Azure Windows virtual machine activation problems](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems)
* Azure Support Team Blog post- [Troubleshooting Windows activation failures on Azure VMs](https://blogs.msdn.microsoft.com/mast/2017/06/14/troubleshooting-windows-activation-failures-on-azure-vms/)<br>
* [Automatic VM Activation (AVMA)](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn303421(v=ws.11)) for Windows Server 2012 R2 and newer versions
* [MAK activation](https://docs.microsoft.com/previous-versions/tn-archive/ff793438(v=technet.10)) for Windows Server 2012 and earlier versions