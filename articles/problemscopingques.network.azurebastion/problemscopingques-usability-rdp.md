<properties
	articleId="problemscopingques-usability-rdp"
	pageTitle="Have trouble using my RDP session or not responding as expected"
	description="Have trouble using my RDP session or not responding as expected"
	authors="spacest"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32641421"
	productPesIds="16757"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureBastion"
/>
# Have trouble using my RDP session or not responding as expected
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Have trouble using my RDP session or not responding as expected",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "name_and_IP",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the name and IP address of the target VM?",
            "required": false
        },
        {
            "id": "browser",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What browser are you using?",
            "required": false
        },
        {
            "id": "browser_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What browser version are you using?",
            "required": false
        },
        {
            "id": "OS",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What OS is your browser running on?",
            "required": false
        },
		{
            "id": "keyboard",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What keyboard layout are you using?",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
        }
---
