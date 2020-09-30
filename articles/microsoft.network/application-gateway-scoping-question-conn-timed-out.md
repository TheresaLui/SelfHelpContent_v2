<properties
	pageTitle="Scoping questions for Application Gateway connection timed out"
	description="Scoping questions for Application Gateway connection timed out"
	authors="surajmb"
	ms.author="surmb"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32639114"
	productPesIds="15922"
	cloudEnvironments="public,fairfax,mooncake,blackforest,usnat,ussec"
	schemaVersion="1"
	articleId="appgw-scoping-question-conn-timed-out"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Scoping questions for Application Gateway connection timed out
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
            "id": "conn_check",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you verified if the traffic to Application Gateway is not blocked by NSG/UDR and if you have configured the listener/rule for the frontend port?",
            "infoBalloonText": "See <a href='https://docs.microsoft.com/azure/application-gateway/configuration-overview#network-security-groups-on-the-application-gateway-subnet'>NSG considerations</a> for more information on troubleshooting",
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
