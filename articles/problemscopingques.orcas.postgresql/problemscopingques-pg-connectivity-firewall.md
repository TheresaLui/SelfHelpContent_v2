<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639982, 32780964, 32731219"
	productPesIds="16222,17067,17068"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-pg-connectivity-firewall"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Database Connectivity - Firewall rules or VNETs
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Connectivity",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Connectivity Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Following the steps in Recommended Solution section below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "persistent_or_intermittent",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the issue persistent or intermittent?",
            "dropdownOptions": [
                {
                    "value": "persistent",
                    "text": "Persistent"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Intermittent"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "intermittent",
            "order": 4,
            "visibility": "persistent_or_intermittent == dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "How often does this issue happen?",
            "dropdownOptions": [
                {
                    "value": "Everyday",
                    "text": "Everyday"
                },
                {
                    "value": "Several times a week",
                    "text": "Several times a week"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "vnet",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you facing issues while connecting from VNET?",
            "infoBalloonText": "VNET is not supported on Basic Tiers.",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "vnet_rule",
            "order": 6,
            "visibility": "vnet == Yes",
            "controlType": "dropdown",
            "displayLabel": "Did you setup a VNET rule for your server?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "firewall_rule",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Did you setup firewall rules on the server?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "No"
                }
            ],
            "required": true,
			"diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any driver exceptions/error messages you received and any other information you want to share with us.",
            "required": true,
			"diagnosticInputRequiredClients": "Portal",
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
