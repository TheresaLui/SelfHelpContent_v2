<properties
	pageTitle="SignalR service self help for data-plane issues"
	description="SignalR service self help for data-plane issues"
	ms.author="lianwei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32683986,32683987,32683988,32683989,32683990,32683991,32683997,32683966,32683967,32683968,32683994,32683976,32683969,32683979,32683980,32683992,32683978"
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
            "infoBalloonText": "Choose how it happens",
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
            "infoBalloonText": "Is the issue still occurring?",
            "dropdownOptions": [
                {
                    "value": "Error_1",
                    "text": "Still occurring"
                },
                {
                    "value": "Error_2",
                    "text": "Automatically recovered"
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
        }
    ]
}
---