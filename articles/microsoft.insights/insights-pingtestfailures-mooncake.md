<properties 
    pageTitle="My web test is intermittently failing with a protocol violation error"
    description="My web test is intermittently failing with a protocol violation error"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    ms.author="mcosner"
    displayOrder="12"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    cloudEnvironments="MoonCake"
 	articleId="insights-pingtestfailures-mooncake"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# My web test is intermittently failing with a protocol violation error

## **Recommended Steps**

The error ("protocol violation.. CR must be followed by LF") indicates an issue with the server (or dependencies). To summarize, this happens when malformed headers are set in the response (this can be caused by load balancers or CDN's). Specifically, some headers might not be using CRLF to indicate end-of-line, which is against the HTTP specification and, therefore, they fail validation at the .NET WebRequest level.  See [this blog post](http://mehdi.me/a-tale-of-debugging-the-linkedin-api-net-and-http-protocol-violations/) for a detailed explanation of the issue. We recommend taking a close look at the network response and try to spot the headers which might be in violation.

Note: The URL may not fail in browsers most likely because they’re implemented with libraries which have a relaxed validation concerning HTTP headers. The blog post above shows examples of this.

## **Recommended Documents**

* [Debug protocol violation errors](http://mehdi.me/a-tale-of-debugging-the-linkedin-api-net-and-http-protocol-violations/)
* [Understand common questions and problems with availability tests](https://docs.azure.cn/azure-monitor/app/monitor-web-app-availability#qna)
