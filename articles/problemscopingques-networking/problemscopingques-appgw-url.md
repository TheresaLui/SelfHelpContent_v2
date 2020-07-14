<properties
	pageTitle="Application Gateway URL"
	description="Application Gateway URL"
	authors="radwiv,spacest"
	ms.author="radwiv,mariliu"
	selfHelpType="problemScopingQuestions"
supportTopicIds="32436964,32582829,32582830,32582826,32582827,32565735,32565736,32582833,32640606,32640607,32640608,32640603,32639117,32639118,32639111,32639112,32639110,32641400,32674895,32674896,32680759,32680758,32680757,32680756"
	productPesIds="15922"
	cloudEnvironments="public,fairfax,mooncake,blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ad021338-109f-4290-a45e-f7be9d73fe26"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Application Gateway URL
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
            "watermarkText": "Example:http://contoso.com or http://contoso.com:8080",
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
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your issue including error messages.",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 5,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/application-gateway/'>Learn more</a> about Application Gateway, including How to setup and troubleshooting steps."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
