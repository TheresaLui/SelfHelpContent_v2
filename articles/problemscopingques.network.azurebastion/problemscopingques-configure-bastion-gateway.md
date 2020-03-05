<properties
	articleId="problemscopingques-configure-bastion-gateway"
	pageTitle="Configure Bastion gateway"
	description="Configure Bastion gateway"
	authors="spacest"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32641415"
	productPesIds="16757"
	cloudEnvironments="public, Fairfax"
	schemaVersion="1"
	ownershipId="CloudNet_AzureBastion"
/>
# Configure Bastion gateway
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Configure Bastion gateway",
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
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
        }
---
