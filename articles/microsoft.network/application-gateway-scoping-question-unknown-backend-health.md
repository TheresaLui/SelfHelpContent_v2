<properties
	pageTitle="Scoping questions for Application Gateway unknown backend health"
	description="Scoping questions for Application Gateway unknown backend health"
	authors="surajmb"
	ms.author="surmb"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32639116"
	productPesIds="15922"
	cloudEnvironments="public,fairfax,mooncake,blackforest,usnat,ussec"
	schemaVersion="1"
	articleId="appgw-scoping-question-unknown-backend-health"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Scoping questions for Application Gateway unknown backend health
---
{
    "subscriptionRequired": true,
	"resourceRequired": true,
    "title": "Application Gateway URL",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "ApplicationGatewayAccessURL",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the URL you are using to access the Application Gateway in the format protocol://domainNameOrIPAddress:portNumber. Port number is not required if you are using standard ports 80 and 443.",
            "watermarkText": "Example: http://contoso.com or http://contoso.com:8080",
            "required": true
        },
				{
            "id": "sku_version",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the SKU version of your Application Gateway?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Standard",
                    "text": "Standard"
                },
                {
                    "value": "WAF",
                    "text": "WAF"
                },
                {
                    "value": "Standard_v2",
                    "text": "Standard_v2"
                },
                {
                    "value": "WAF_v2",
                    "text": "WAF_v2"
                },
				{
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "nsgudr_check",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you verified if the traffic to Application Gateway on ports 65200-65535 are not blocked by NSG/UDR or default route advertised via BGP?",
            "infoBalloonText": "See <a href='https://docs.microsoft.com/azure/application-gateway/application-gateway-backend-health-troubleshooting#backend-health-status-unknown'>Unknown backend health</a> for more information on troubleshooting the issue",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
