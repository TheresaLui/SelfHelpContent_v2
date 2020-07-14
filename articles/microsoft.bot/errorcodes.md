<properties
	pageTitle="Bot is returning errors"
	description="Bot is returning errors"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-danava,jiruss,dandris,saziz"
	displayOrder="107"
	selfHelpType="resource"
	supportTopicIds="32688623,32688619"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="D232159F-90F9-4A4A-A5D5-A109D55A3218"
	ownershipId="Compute_BotService"
/>
# Bot is returning errors

## **Recommended Steps**

### **General**

Sending and receiving bot messages involves many components: a client application (such as Teams or Web Chat), intermediate servers, and the bot's cloud endpoint. Any of these components can generate error codes if they are misconfigured or functioning incorrectly. This guide will help you understand the meaning of these error codes.

You can make use of Application Insights to be able to debug why the bot is responding with an error. Visit the below link on how to use Application Insights: 

* [Diagnose run-time exceptions with Application Insights](https://docs.microsoft.com/azure/azure-monitor/learn/tutorial-runtime-exceptions)

### **HTTP 401 and 403**

HTTP 401 indicates that the client, bot, or channel are not sending their credentials or tokens. HTTP 403 indicates that the credentials are received but are not allowed for the current operation. Some reasons for these errors are:

* The bot's Microsoft Application ID or Password are not correct in the bot's configuration
* Credentials (e.g. Facebook page ID and password) are not correct in the bot's Azure Bot Service registration
* The client, such as Web Chat, is using an expired token
* If using the C# Bot Builder SDK to send proactive messages, the bot's source code does not call TrustServiceUrl to allow tokens to be sent to a corresponding service

[More information](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-authentication-problems?view=azure-bot-service-4.0)

### **HTTP 404**

An HTTP 404 error from a web API indicates the request was incorrect. In some cases, an HTTP 404 occurs when a caller does not supply the required credential or token information. Some HTTP 404s are benign. Requests for favicon.ico can be ignored.

Some causes for HTTP 404s include:

* Incorrectly setting the bot's endpoint to a path that is not recognized by the bot
* Incorrect tokens or credentials (see section on HTTP 401 and 403 above)

### **HTTP 405**

HTTP 405 errors typically occur when a bot's endpoint is incorrectly configured. Inspect the bot's endpoint configuration in the Azure Bot Service registration and make sure it matches your bot's source code. Most bots use an HTTP request path of `/api/messages`.

### **HTTP 409 and 412**

HTTP 409 and 412 indicate that a data collision occurred. This happens most frequently inside bots (v3 only) when they receive multiple user requests and try to process them in parallel, resulting in ambiguous conversation state.

[More information](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-general-problems?view=azure-bot-service-4.0#what-causes-an-error-with-http-status-code-412-precondition-failed-or-http-status-code-409-conflict)

### **HTTP 429**

An error response with HTTP status code 429 indicates that too many requests have been issued in a given amount of time. The body of the response typically includes an explanation of the problem and may also specify the minimum required interval between requests.

Bots, client, and other HTTP callers that receive a 429 should honor any included `Retry-After` HTTP header in the response.

There are three likely causes for a 429 error:

* If you're using the ngrok tool for debugging your bot, it will generate 429s. See ngrok documentation for more details.
* Old versions of the Web Chat library can create traffic that result in 429s from the services they contact. If using Web Chat, upgrade to the latest version.
* If 429s are observed as part of a test conducted against the Direct Line service, this is expected. Direct Line is optimized for human conversation and will emit 429s in response to load tests.

More information:

* [HTTP 429 Error](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-general-problems?view=azure-bot-service-4.0#what-causes-an-error-with-http-status-code-429-too-many-requests)
* [Rate limiting](https://docs.microsoft.com/azure/bot-service/bot-service-resources-bot-framework-faq?view=azure-bot-service-4.0#rate-limiting)

### **HTTP 500**

An HTTP 500 indicates an internal, unknown failure. If a bot returns an HTTP 500, some causes include:

* A possible configuration error, such as an incorrect or missing Microsoft App password
* Missing libraries
* An internal logic error

Many HTTP 500 errors are accompanied by an HTTP body describing the error.

[More information](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-500-errors?view=azure-bot-service-4.0&tabs=dotnetwebapi)

### **HTTP 502**

The Direct Line service returns HTTP 502 to communicate that it tried to contact the bot, but the bot returned an error or did not acknowledge the request in time.

### **HTTP 503**

An HTTP 503 indicates that the recipient of the request was unable to receive or process it. This can be caused by a service outage (either an Azure service or the bot itself) or it can be due to a client that is unable to contact a service, which then synthesizes an HTTP 503 to represent the error.

HTTP 503 errors are often transient, although deeper investigation into which component is causing the problem will help narrow further troubleshooting.

## **Recommended Documents**

* [HTTP Status codes for Directline API](https://docs.microsoft.com/azure/bot-service/rest-api/bot-framework-rest-direct-line-3-0-api-reference?view=azure-bot-service-4.0#http-status-codes)
