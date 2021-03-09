<properties
  pagetitle="User Verification! Hostname in certificate didn’t match&#xD;"
  service="microsoft.cognitiveservices"
  resource="accounts"
  ms.author="jtanner,saziz,enesu"
  selfhelptype="Resource"
  supporttopicids="32589913,32589914,32589915,32589916,32589918,32589919,32589920,32589921,32589922,32589923,32589925,32589927,32589930,32589932,32589936,32589938,32589940,32589941,32589942,32592300,32589911"
  resourcetags=""
  productpesids="16121"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="6c452c93-a5fd-4bbb-b205-75d6750f02d7"
  ownershipid="AzureCogSvc_CognitiveServices" />
# User Verification! Hostname in certificate didn’t match

Use these steps to resolve errors about User Verification and the certification not matching when calling a Cognitive Service.
 
For example:

"User Verification! hostname in certificate didn't match: <centralIndia.api.cognitive.microsoft.com> != <*.cognitiveservices.azure.com> OR <*.cognitiveservices.azure.com>"

The domain name **.cognitiveservices.azure.com** was recently added for Cognitive Services. It is set to the default SSL binding certificate. This means, if an SNI header is missing, API management will use the default certificate which is now **.cognitiveservices.azure.com**.
 
## **Recommended Steps**

Change your SNI header to specify `yourregion.api.cognitive.microsoft.com` domain for TLS/SSL handshakes going forward. In the example error, the correct syntax would be `centralIndia.api.cognitive.microsoft.com`.
 
## **Recommended Documents**

* [How APIM Proxy Server responds with SSL certificates in the TLS handshake](https://docs.microsoft.com/azure/api-management/configure-custom-domain#clients-calling-without-sni-header)
