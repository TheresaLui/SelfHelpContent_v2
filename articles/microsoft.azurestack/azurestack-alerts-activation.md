<properties
    pageTitle="Azure Stack VM Activation"
    description="General guidance for Azure Stack alert issues"
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

Windows products must be used in accordance with Product Use Rights and Microsoft license terms. Azure Stack uses [Automatic VM Activation (AVMA)](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn303421(v=ws.11)) to activate Windows Server virtual machines (VMs).

## **Recommended Steps**

1. Azure Stack host activates Windows with AVMA keys for Windows Server 2016. All VMs that run Windows Server 2012 R2 or later are automatically activated.
2. VMs that run Windows Server 2012 or earlier are not automatically activated and must be activated by using [MAK activation](https://docs.microsoft.com/previous-versions/tn-archive/ff793438(v=technet.10)), using your own product key.
3. Microsoft Azure uses KMS activation to activate Windows VMs. 
4. If you move a VM from Azure Stack to Azure and encounter activate problems, see [Troubleshoot Azure Windows virtual machine activation problems](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems).

## **Recommended Documents**

* [Troubleshoot Azure Windows virtual machine activation problems](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-activation-problems)
* Azure Support Team Blog post- [Troubleshooting Windows activation failures on Azure VMs](https://blogs.msdn.microsoft.com/mast/2017/06/14/troubleshooting-windows-activation-failures-on-azure-vms/)<br>
* [Automatic VM Activation (AVMA)](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn303421(v=ws.11)) for Windows Server 2016 and newer
* [MAK activation](https://docs.microsoft.com/previous-versions/tn-archive/ff793438(v=technet.10)) for Windows Server 2012 and earlier