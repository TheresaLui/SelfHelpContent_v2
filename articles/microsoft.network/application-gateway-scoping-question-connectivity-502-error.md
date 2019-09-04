<properties
	pageTitle="Scoping questions for Application Gateway issues for Connectivity/502 error"
	description="Scoping questions for Application Gateway issues for Connectivity/502 error"
	authors="abshamsft"
	ms.author="absha"
	selfHelpType="problemScopingQuestions"
supportTopicIds="32573483"
	productPesIds="15922"
	cloudEnvironments="public,fairfax,mooncake,blackforest"
	schemaVersion="1"
	articleId="scoping-question-connectivity-502-error"
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
        "description": "Our Application Gateway Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource."
    },
    "formElements": [
        {
            "id": "ApplicationGatewayAccessURL",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the URL you are using to access the Application Gateway in the format protocol://domainNameOrIPAddress:portNumber. Port number is not required if you are using standard ports 80 and 443.",
            "watermarkText": "Example:http://contoso.com or http://contoso.com:8080",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "backend_health",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are there any [Unhealthy backends](data-blade:Microsoft_Azure_Network.ApplicationGatewayBackendHealthGridBlade)?",
            "watermarkText": "Choose an option",		
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
