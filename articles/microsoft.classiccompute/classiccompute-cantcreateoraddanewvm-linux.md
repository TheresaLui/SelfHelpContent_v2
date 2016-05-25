<properties 
    pageTitle="I can't create or add a new VM" 
    description="I can't create or add a new VM" 
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="kasparks"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="linux"
    productPesIds=""	 
 />
    
# I can't create or add a new VM

## **Recommended steps**
1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the failure reason
2. Look up suggested actions by error code <br>
[Troubleshoot error codes for create or add a new VM](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/#error-string-lookup)
3. Try your request using a smaller VM size or a different cloud service. Use the following article if you're using a different cloud service. <br>
[Configure regional Virtual Network to connect Cloud services](https://azure.microsoft.com/blog/vnet-to-vnet-connecting-virtual-networks-in-azure-across-different-regions/)
4. If you're creating a new VM using a custom image, review the following article to verify that you followed the necessary steps to create the image <br>
[How to capture a classic Linux virtual machine as an image](https://azure.microsoft.com/documentation/articles/virtual-machines-linux-capture-image/)

## **Recommended documents**
[Troubleshooting allocation failure when you create, restart or resize a VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-allocation-failure/)
