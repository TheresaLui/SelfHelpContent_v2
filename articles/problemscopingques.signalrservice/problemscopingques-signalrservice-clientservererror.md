<properties
	pageTitle="SignalR service self help for data-plane issues"
	description="SignalR service self help for data-plane issues"
	ms.author="lianwei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32683986,32683987,32683988,32683989,32683990,32683991,32683997,32683966,32683967,32683968,32683994,32683976,32683969,32683979,32683980,32683992,32683978"
	productPesIds="16477"
	cloudEnvironments="public,Mooncake,Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-signalrservice-clientservererror"
	ownershipId="SignalRService_Triage"
/>
# Can't apply this label
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SignalR service self help for data-plane issues",
    "fileAttachmentHint": "Please upload both the client-side and server-side log files, <a href='https://docs.microsoft.com/azure/azure-signalr/signalr-howto-troubleshoot-method'>here</a> contains more detail on how to.",
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
            "id": "occur_dropdown",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue still occurring?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose how it happens",
            "dropdownOptions": [
                {
                    "value": "Error_1",
                    "text": "Still occurring"
                },
                {
                    "value": "Error_2",
                    "text": "Occurs from time to time"
                },
                {
                    "value": "Error_3",
                    "text": "Recovered automatically"
                },
                {
                    "value": "Error_4",
                    "text": "Recovered by creating another service"
                },
                {
                    "value": "Error_5",
                    "text": "Recovered by ad-hoc steps (specify below, e.g. restart the app server, restart the service, use an old version SDK, etc.)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "adhoc_stps",
            "order": 3,
            "visibility": "occur_dropdown == Error_5",
            "controlType": "textbox",
            "displayLabel": "Ad-hoc steps taken to recover the service",
            "infoBalloonText": "Please specify the ad-hoc steps taken that recovered the service, e.g. restart the app server, restart the service, use an old version SDK, etc.",
            "required": true
        },
        {
            "id": "customer_impact",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Any customer impact?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Any customer impact?",
            "dropdownOptions": [
                {
                    "value": "Error_1",
                    "text": "No, there is no customer impact."
                },
                {
                    "value": "Error_2",
                    "text": "Some of our customers are impacted"
                },
                {
                    "value": "Error_3",
                    "text": "All our customers are impacted"
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
            "required": true,
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