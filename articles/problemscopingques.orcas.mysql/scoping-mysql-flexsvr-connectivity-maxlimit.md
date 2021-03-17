<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747638"
	productPesIds="17344"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-mysql-flexsvr-connectivity-maxlimit"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Connectivity - Server hit maximum connection limit
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Connectivity",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "persistent_or_intermittent",
            "order": 2,
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
            "required": true
        },
        {
            "id": "intermittent",
            "order": 3,
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
            "id": "connection_pooler",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you using a connection pooler?",
            "infoBalloonText": "It is highly recommended to use a connection pooler while connecting to the server.",
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
            "required": true
        },
        {
            "id": "connection_pooler_type",
            "order": 5,
            "visibility": "connection_pooler == Yes",
            "controlType": "textbox",
            "displayLabel": "What connection pooler are you using?",
            "required": false
        },
        {
            "id": "connection_pooler_config",
            "order": 6,
            "visibility": "connection_pooler == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Could you provide connection pooling configuration?",
            "required": false
        },
        {
            "id": "workload",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What does your workload look like?",
            "dropdownOptions": [
                {
                    "value": "Mostly reads",
                    "text": "Mostly reads"
                },
                {
                    "value": "Mostly writes",
                    "text": "Mostly writes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Mix of both"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any driver exceptions/error messages you received and any other information you want to share with us.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
