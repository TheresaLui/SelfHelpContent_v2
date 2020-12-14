<properties
	pageTitle="SignalR service self help for control-plane issues"
	description="SignalR service self help for control-plane issues"
	ms.author="lianwei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608605,32684005"
	productPesIds="16477"
	cloudEnvironments="public,Mooncake,Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-signalrservice-control-plane-occur"
	ownershipId="SignalRService_Triage"
/>
# Can't apply this label
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SignalR service self help for control-plane issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "error_dropdown",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "How does it happen?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Error_1",
                    "text": "It happens from the very beginning, it never works."
                },
                {
                    "value": "Error_2",
                    "text": "It happens after we upgraded the SDK version."
                },
                {
                    "value": "Error_3",
                    "text": "It suddenly happens, it worked well before."
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "error_occur",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the issue still occurring?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Error_1",
                    "text": "Still occurring"
                },
                {
                    "value": "Error_2",
                    "text": "Automatically recovered"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 50,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        }
    ]
}
---