<properties
	articleId="problemscopingques-i-cannot-view-activity-log-in-log-analytics"
	pageTitle="I can't view Activity Log in Log Analytics"
	description="I can't view Activity Log in Log Analytics"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684685"
	productPesIds="16251"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>

# I can't view Activity Log in Log Analytics
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "I can't view Activity Log in Log Analytics",
    "fileAttachmentHint": "If possible, please upload screenshots of the issue and additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
        {
            "id": "problem_descriptionla",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the Log Analytics workspace name and the Azure subscription id where it exists.",
            "watermarkText": "Provide the Log Analytics workspace name and the Azure subscription id where it exists.",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of exactly what you are trying to view in Log Analytics.",
            "watermarkText": "Provide details of exactly what you are trying to view in Log Analytics.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Provide the Log Analytics query being executed"
                },
                {
                    "text": "Provide details of results you are expecting"
                },
                {
                    "text": "If possible, attach a screenshot of the error"
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
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---