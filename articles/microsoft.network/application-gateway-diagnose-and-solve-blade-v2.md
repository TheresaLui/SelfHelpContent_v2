<properties
pageTitle="Top common problems for Application Gateway"
description="Menu based workflow document for top Application Gateway problems"        
service="microsoft.network"
resource="applicationgateways"
authors="abshamsft"
ms.author="absha"
displayOrder=""
articleId="application-gateway-diagnose-and-solve-v2"
selfHelpType="diagnoseandsolve"
resourceTags=""
productPesIds="15922"
cloudEnvironments="public"
/>
# Diagnose and solve v2 sample article for application gateway
---
{
  "$schema": "SelfHelpContent",
  "commonProblems": [
    {
      "id": "connectivity_issues",
      "title": "I'm encountering connectivity issues",
      "description": "When trying to access the application gateway domain, I'm encountering connectivity issues ",
      "category": "Connectivity",
      "searchTags": "202, bad gateway, server, error, 400, 403, 404, client, redirect, err_too_many_redirects, connection, timed out, unknown",
      "supportTopicId": "32436961",
      "subProblems": [
        {
          "id": "Im_encountering_Bad_Gateway_Error_(502)",
          "title": "I'm encountering Bad Gateway Error (502)",
          "description": "When trying to access the application gateway domain, I'm encountering the following error: Server Error: 502 - Web server received an invalid response while acting as a gateway or proxy server.",
          "supportTopicId": "32573483",
          "commonSolutionArticleId": "application-gateway-502-error",
          "symptomId": ""
        },
        {
          "id": "Im_encountering_4xx_client_error",
          "title": "I'm encountering 4xx client error",
          "description": "When trying to access the application gateway domain, I'm encountering one of the following 4xx client errors: 400 Bad Request, 403 Forbidden, 404 Not Found",
          "supportTopicId": "32639113",
          "commonSolutionArticleId": "application-gateway-4xx-error",
          "symptomId": ""
        },
        {
          "id": "Im_encountering_too_many_redirects",
          "title": "I'm encountering too many redirects",
          "description": "When trying to access the application gateway domain, I'm encountering one of the following errors: redirected you too many times, page isn’t redirecting properly, webpage has a redirect loop, etc. ",
          "supportTopicId": "32639115",
          "commonSolutionArticleId": "application-gateway-too-many-redirects-error",
          "symptomId": ""
        },
        {
          "id": "Im_encountering_connection_timed_out_error",
          "title": "I'm encountering connection timed out error",
          "description": "When trying to access the application gateway domain, I'm encountering Connection timed out error.",
          "supportTopicId": "32639114",
          "commonSolutionArticleId": "application-gateway-unknown-backend-health",
          "symptomId": ""
        },
        {
          "id": "Im_encountering_connection_timed_out_error",
          "title": "I'm encountering connection timed out error",
          "description": "When viewing the backend health, the backend health status is Unknown.",
          "supportTopicId": "32639117",
          "commonSolutionArticleId": "application-gateway-connection-timed-out-error",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "configuration_issues",
      "title": "I'm encountering issues in configuring the Application Gateway",
      "description": "When trying to configure the application gateway domain, I'm encountering issues ",
      "category": "Configuration and Setup",
      "searchTags": "SSL, HTTPS, encryption, end, whitelist, certificate",
      "supportTopicId": "32436961",
      "subProblems": [
        {
          "id": "SSL_termination",
          "title": "SSL termination",
          "description": "SSL termination is not working properly.",
          "supportTopicId": "32582828",
          "commonSolutionArticleId": "application-gateway-ssl-termination",
          "symptomId": ""
        },
        {
          "id": "End-to-end_SSL",
          "title": "End-to-end SSL",
          "description": "End-to-end SSL encryption is not working properly.",
          "supportTopicId": "32582825",
          "commonSolutionArticleId": "application-gateway-end-to-end-ssl",
          "symptomId": ""
        }
      ]
    },
    {
      "id": "session_affinity",
      "title": "Session Affinity",
      "description": "I'm encountering session affinity issues while the traffic is directed from the Application Gateway to the backend.",
      "category": "Routing",
      "searchTags": "cookie, session affinity, cookie-based",
      "supportTopicId": "32640605",
      "commonSolutionArticleId": "application-gateway-session-affinity",
      "symptomId": ""
    }
  ],
  "troubleshootingTools": [
    {
      "id": "Troubleshoot_backend_connectivity_issues",
      "title": "Troubleshoot backend connectivity issues",
      "description": "Use Connection Toubleshoot to check network performance and connectivity issues while connecting from the Application Gateway to your backend servers",
      "category": "Connectivity",
      "searchTags": "backend",
      "type": "tool",
      "bladeLink": {
        "extensionName": "Microsoft_Azure_Network",
        "bladeName": "NetworkWatcherConnectivityBlade",
        "parameters": [
          {
            "name": "id",
            "value": "$resourceId"
          }
        ]
      }
    }
  ]
}
---
