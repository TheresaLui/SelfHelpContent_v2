<properties
	pageTitle="Security"
	description="Scoping questions to capture more details about Security "
	authors="meetshamir"
	ms.author="saziz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688659"
	productPesIds="16152"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="9ADEAAF2-03BE-45CD-9E31-AE1B04511877"
	ownershipId="Compute_BotService"
/>
# Security 
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Security ",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
			{
			"id": "advice",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What do you need help on?",
			"dropdownOptions": [{
					"value": "5a",
					"text": "Single Sign-on or Authentication"
				}, {
					"value": "5b",
					"text": "Protection against attack - DDOS/Port Scanning/IP Spoofing etc/Man in the middle"
				}, {
					"value": "5c",
					"text": "Security best practices"
				}, {
					"value": "5d",
					"text": "Vulnerability test results or reporting a vulnerability"
				}, {
					"value": "5e",
					"text": "Controlling access to a bot"
				}, {
					"value": "5f",
					"text": "Firewall/Gateway/Proxy configuration"
				}
				, {
					"value": "5g",
					"text": "Others"
				},
				{
					"value": "dont_know_answer",
					"text": "Don't know"
				}
			],
			"required": true
		},
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details, if you see an error message list it or you are looking for specific guidance.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide as much details as possible"
        }
	]
}
---
