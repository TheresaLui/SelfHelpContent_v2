<properties
	articleId="problemscopingques-expected-information-is-missing-in-the-log"
	pageTitle="Expected information is missing in the log"
	description="Expected information is missing in the log"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684691"
	productPesIds="16251"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>
# Expected information is missing in the log
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Expected information is missing in the log",
    "fileAttachmentHint": "If possible, please upload screenshots and additional attachments which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of the Activity Log event.",
            "watermarkText": "Provide details of the Activity Log event.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Provide the operation name for the expected events"
                },
                {
                    "text": "Provide the timestamp and time zone of when the events were expected"
                },
                {
                    "text": "Provide a copy/paste of the event JSON"
                }
            ]
        },
            {
            "id": "expected_information",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of what was expected but is missing from the event.",
            "watermarkText": "Provide details of what was expected but is missing from the event.",
            "required": true,
            "useAsAdditionalDetails": false
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