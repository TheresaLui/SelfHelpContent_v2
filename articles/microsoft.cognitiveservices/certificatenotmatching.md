<properties
        pageTitle="User Verification! Hostname in certificate didn’t match"
        description="Error received about User Verification due to certificate issue"
        service="microsoft.cognitiveServices"
        resource="accounts"
        authors="jtanner-msft,meetshamir"
        ms.author="jtanner,saziz"
        displayOrder="35"
        selfHelpType="resource"                         supportTopicIds="32589913,32589916,32589918,32589919,32589920,32589921,32589922,32589923,32589924,32589925,32589927,32589930,32589932,32589936,32589938,32589940,32589911,32592300,32589914,32589941,32589942,32589915"
        resourceTags=""
        productPesIds="16121"
        cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
        articleId="6c452c93-a5fd-4bbb-b205-75d6750f02d7"
	ownershipId="AzureCogSvc_CognitiveServices"
/>

# User Verification! Hostname in certificate didn’t match

Issue: When calling a Cognitive Service you receive an error about User Verification and the certification not matching.
 
An example of the reported error:

User Verification! hostname in certificate didn't match: <centralIndia.api.cognitive.microsoft.com> != <*.cognitiveservices.azure.com> OR <*.cognitiveservices.azure.com>

“*.cognitiveservices.azure.com” is a domain name that was recently added for Cognitive Services. It is set to the default SSL binding certificate so if an SNI header is missing, API management will use the default certificate which is “*.cognitiveservices.azure.com” now.
 
## **Recommended Steps**

Change your SNI header to specify 'yourregion.api.cognitive.microsoft.com' domain for TLS/SSL handshakes going forward. In the example error, the correct syntax would be "centralIndia.api.cognitive.microsoft.com".
 
## **Recommended Documents**

* [How APIM Proxy Server responds with SSL certificates in the TLS handshake](https://docs.microsoft.com/azure/api-management/configure-custom-domain#clients-calling-without-sni-header)
