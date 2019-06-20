<properties
    pageTitle="I can’t access my device in File Explorer"
    description="I can’t access my device in File Explorer"
    service="microsoft.databoxedge"
    resource="databoxedgedevices"
    authors="anoobbacker"
    ms.author="anbacker"
    authoralias="anbacker"
    displayOrder="10"
    articleId="16e2c6f3-c6b2-42d6-b8ec-853c5eaeae61"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="DataBoxGateway"
    productPesIds=""
    cloudEnvironments="public"
/>

# I can’t access my device in File Explorer

## **Recommended Steps**

If you can't access your device in File Explorer, try the following:

1. In the Azure portal, check if your device shows offline
2. In the local web UI of the device, go to **Troubleshooting** > **Diagnostic tests** and click **Run diagnostic tests**. Resolve any reported issues.
3. If you are accessing your device via the IP, check if you have used DHCP instead of a static IP. Your IP may have changed.
4. Check the Hyper-V or ESX host for your VM to make sure that the VM is turned on and running

## **Recommended Documents**

* [Troubleshoot your Azure Data Box Gateway issues](https://docs.microsoft.com/azure/databox-online/data-box-gateway-troubleshoot)
