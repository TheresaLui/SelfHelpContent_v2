<properties
    pageTitle="HTTPS customized certificate upload timeout/failed"
    description="HTTPS customized certificate upload timeout/failed"
    service="microsoft.cdn"
    resource="profiles"
    authors="huaiyizhu"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="cdnakamai, cdnverizon"
    productPesIds=""
    cloudEnvironments="Mooncake"
	articleId="433756f8-2963-48b7-a3e7-22e0427f0d88"
	ownershipId="CloudNet_ContentDeliveryNetwork"
/>

# HTTPS customized certificate upload timeout/failed

## **Recommended steps**
1. Check if length of the certificate encryption is 2048-bit. Our background only supports 2048-bit certificate upload. For other lengths, please convert to 2048-bit or contact support for offline configuration.

2. Check if the certificate is in PEM format. Our background only supports PEM format certificate upload. For other formats, please convert to PEM format or contact support for offline configuration.

3. Check if the certificate is normal and with associated certificate chain. If the certificate contains both root and intermediate authority, please have them combined and uploaded to ensure the certificate can be fully validated.

4. If your situation doesn't apply to above 1 to 3, please [contact support](https://www.azure.cn/support/contact/) for help.