<properties
	articleId="problemscopingques-i-cannot-find-the-logs-for-expected-event"
	pageTitle="I cannot find the logs for expected event"
	description="I cannot find the logs for expected event"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684695"
	productPesIds="16251"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>
# I cannot find the logs for expected event
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "I cannot find the logs for expected event",
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
            "displayLabel": "Provide details of events that were expected.",
            "watermarkText": "Provide details of events that were expected.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Provide the resources related to the expected events"
                },
                {
                    "text": "Provide the operation name for the expected events"
                },
                {
                    "text": "Provide the timestamp and time zone of when the events were expected"
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 6,
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