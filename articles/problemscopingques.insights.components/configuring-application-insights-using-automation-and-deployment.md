<properties
	articleId="configuring-application-insights-using-automation-and-deployment"
	pageTitle="Configuring Application Insights using automation and deployment"
	description="Configuring Application Insights using automation and deployment"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729590, 32729591"
	productPesIds="15693"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Configuring Application Insights using automation and deployment
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configuring Application Insights using automation and deployment",
    "fileAttachmentHint": "Please uploaded the relevant code and any other information which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
         {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the problem you are seeing",
            "watermarkText": "Please include expected versus observed behavior, exact errors, etc",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide expected versus observed behavior"
                },
                {
                    "text": "Provide the exact errors"
                },
                {
                    "text": "Upload screenshots below as additional file attachments"
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---