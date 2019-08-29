<properties
	pageTitle="Unexpected increase in resource consumption"
	description="Scoping questions to capture more details about Performance and Query Execution\Unexpected increase in resource consumption"
	authors="keithelm"
	ms.author="keithelm,devinr"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630459"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="B74000CE-E6CD-4996-8241-AE8C0B6476DD"
/>
# Error When Connecting to my Database
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Performance and Query Execution\\Unexpected increase in resource consumption",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the performance problem.",
            "required": true
       },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the problem stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
        {
            "id": "resource_with_increase",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What resource type has increased consumption?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "What resource type did you observe with increased consumption?",
            "dropdownOptions": [
                {
                    "value": "cpu_increased",
                    "text": "CPU usage"
                },
                {
                    "value": "io_increased",
                    "text": "IO usage"
                },
                {
                    "value": "memory_increased",
                    "text": "Memory usage"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other/Don't know"
                }
            ],
            "required": false
        },
        {
            "id": "any_known_changes",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have there been any recent changes?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Please indicate what status Resource Health reports for your database or elastic pool.",
            "dropdownOptions": [
                {
                    "value": "no_changes",
                    "text": "No recent Changes"
                },
                {
                    "value": "new_app_schema",
                    "text": "Yes, a new version of the app/schema was recently deployed"
                },
                {
                    "value": "changed_slo",
                    "text": "Yes, we changed service tiers/DTUs"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unknown/I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional context to help us solve your issue.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "On the Basics tab, please ensure you selected a server, database or elastic pool in the Resource dropdown so we know what resource you need assistance with.  Add any additional details that may help us troubleshoot your issue."
        }
    ]
}
---
