<properties
	articleId="problemscopingques-configure-delete-gateway"
	pageTitle="Delete Bastion gateway"
	description="Delete Bastion gateway"
	authors="spacest"
	ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32641416"
	productPesIds="16757"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureBastion"
/>
# Delete Bastion gateway
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Delete Bastion gateway",
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
            "id": "reason",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the reason for your deleting the Azure Bastion resource?",
            "required": false
        },
		{
            "id": "expensive",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Did you find the Azure Bastion service to be expensive?",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
        }
---
