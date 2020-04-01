<properties
    pageTitle="Files cannot be cached after configuring CDN"
    description="Files cannot be cached after configuring CDN"
    service="microsoft.cdn"
    resource="profiles"
    authors="huaiyizhu"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="cdnakamai, cdnverizon"
    productPesIds=""
    cloudEnvironments="Mooncake"
	articleId="a34ce91e-45ec-487b-ba38-b1c2c9d6a560"
	ownershipId="CloudNet_ContentDeliveryNetwork"
/>

# Files cannot be cached after configuring CDN

## **Recommended steps**
1. Please check cache status for a few more times. If the issue still exists, factors like CDN distributed structure, cache timeout or file updating which cause files can't be cached should be excluded.

2. Check if there are cache rules for configuring this type of file. You can check from background cache rules and whether they contain any file type that cannot be cached during test.

3. Check if there is cache rule of "files can't be cached" on top of other rules. Since the rule that is configured first is given the highest priority level, it will cause all the other subsequent rules no longer matched. It's better to put the rule of "files can't be cached" at the bottom(you can also set cache time to 1 second).

4. Please check if "ignore parameter cache" is configured. If access to files requires parameters, and change parameters to access causes cache failure. This may be due to "ignore parameter cache" not turned on. And you should enable "ignore parameter cache". Please refer to [this](https://docs.azure.cn/cdn/cdn-management-portal-how-to-use#domain-name-managementa-idstep2a) for configuration.

5. If your situation doesn't apply to above 1 to 4, please [contact support](https://www.azure.cn/support/contact/) for help.