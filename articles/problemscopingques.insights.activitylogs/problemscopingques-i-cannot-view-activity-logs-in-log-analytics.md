<properties
	articleId="problemscopingques-integration-with-3rd-party-siem-tools"
	pageTitle="Integration with 3rd party SIEM tools"
	description="Integration with 3rd party SIEM tools"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688872"
	productPesIds="16251"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>
# Integration with 3rd party SIEM tools
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Integration with 3rd party SIEM tools",
    "fileAttachmentHint": "If possible, please upload screenshots and additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
        {
            "id": "thirdparty_tool",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What third party tool is being utilized?",
            "watermarkText": "What third party tool is being utilized?",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of the issue you are experiencing and any verbatim error message(s) you are receiving.",
            "watermarkText": "Provide details of the issue you are experiencing and any verbatim error message(s) you are receiving.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Provide details of the kind of integration is being attempted"
                },
                {
                    "text": "Provide timestamp and time zone of at least one instance of the issue occurring"
                },
                {
                    "text": "If possible, attach a screenshot of the issue and any errors"
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