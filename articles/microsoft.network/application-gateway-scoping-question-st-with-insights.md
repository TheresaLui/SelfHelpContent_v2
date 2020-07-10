<properties
	pageTitle="Application Gateway URL"
	description="Application Gateway URL"
	authors="abshamsft"
	ms.author="absha"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32582825,32582828,32640605,32639115,32639109,32639114,32639116,32640602"
	productPesIds="15922"
	cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-question-for-insights"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Application Gateway URL
---
{
    "subscriptionRequired": true,
	"resourceRequired": true,
    "title": "Application Gateway URL",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Application Gateway Access URL",
        "description": "Use our Application Gateway Troubleshooter to troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource."
    },
    "formElements": [
        {
            "id": "ApplicationGatewayAccessURL",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the URL you are using to access the Application Gateway in the format domainNameOrIPAddress:portNumber/urlPath. Port number is not required if you are using standard ports 80 and 443.",
            "watermarkText": "Example:http://contoso.com/abc or http://contoso.com:8080/abc",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
		{
            "id": "ApplicationGatewayAccessProtocol",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please provide Protocol you are using to access Appplication Gateway",
            "watermarkText": "Choose an option from http/https",
            "dropdownOptions": [
                {
                    "value": "http",
                    "text": "http"
                },
                {
                    "value": "https",
                    "text": "https"
                },
				{
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
        },
		{
            "id": "sku_version",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the SKU version of your Application Gateway?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "v1_SKU",
                    "text": "V1 SKU"
                },
                {
                    "value": "v2_SKU",
                    "text": "V2 SKU"
                },
				{
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your issue including error messages.",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 6,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/application-gateway/'>Learn more</a> about Application Gateway, including How to setup and troubleshooting steps."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
