<properties
	pageTitle="Application Gateway URL"
	description="Application Gateway URL"
	authors="radwiv"
	ms.author="radwiv, mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32436964, 32436960,32582828,32582829,32582830,32582825,32582826,32582827,32436961,32573483,32582834,32436962,32565734,32565735,32565736,32582833,32640605,32640604,32640606,32640607,32640608,32640602,32640603,32639113,32639114,32639115,32639116,32639117,32639118,32639111,32639112,32639110,32639109"
	productPesIds="15922"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="ad021338-109f-4290-a45e-f7be9d73fe26"
/>
# Application Gateway URL
---
{
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
            "displayLabel": "Please provide the URL you are using to access the Application Gateway.",
            "watermarkText": "Example: http://www.contoso.com",
            "required": true,
	    "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your issue including error messages.",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 4,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/application-gateway/'>Learn more</a> about Application Gateway, including How to setup and troubleshooting steps."
        }
    ]
}
---
