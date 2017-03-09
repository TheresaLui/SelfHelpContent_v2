<properties
    pageTitle="I need to execute a custom script hosted on a private storage account"
    description="I need to execute a custom script hosted on a private storage account"
    service="scalesets"
    author="negat"
    displayOrder="54"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# I need to execute a custom script hosted on a private storage account. I have no problems when the storage is public but when I try to use a Shared Access Signature(SAS) it fails with the error: “Missing mandatory parameters for valid Shared Access Signature”. I know that link+SAS works fine from my local browser.

You must set up protected settings with the storage account key and name for this scenario to work. See https://azure.microsoft.com/documentation/articles/virtual-machines-windows-extensions-customscript/#template-example-for-a-windows-vm-with-protected-settings
## Networking