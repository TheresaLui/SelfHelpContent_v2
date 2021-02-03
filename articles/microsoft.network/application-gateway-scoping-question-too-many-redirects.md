<properties
	pageTitle="Scoping questions for Application Gateway too many redirects"
	description="Scoping questions for Application Gateway too many redirects"
	authors="surajmb"
	ms.author="surmb"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32639115"
	productPesIds="15922"
	cloudEnvironments="public,fairfax,mooncake,blackforest,usnat,ussec"
	schemaVersion="1"
	articleId="appgw-scoping-question-too-many-redirects"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Scoping questions for Application Gateway too many redirects
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
            "id": "redirect_check",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you verified if Application Gateway is set up with SSL termination and backend server redirects clients on HTTPS?",
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
            "id": "bypass_appgtw_check",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you facing the issue when accessing the backend directly by bypassing the Application Gateway?",
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
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your issue including error messages.",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/application-gateway/'>Learn more</a> about Application Gateway, including How to setup and troubleshooting steps."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
