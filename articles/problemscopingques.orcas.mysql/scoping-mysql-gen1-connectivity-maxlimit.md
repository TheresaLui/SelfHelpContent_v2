<properties
	pageTitle="Database Connectivity"
	description="Database Connectivity"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747586"
	productPesIds="17343"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scoping-mysql-gen1-connectivity-maxlimit"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Database Connectivity - Server hit maximum connection limit
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Connectivity",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for MySQL Connectivity Troubleshooter",
        "description": "Our Azure Database for MySQL Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Follow the steps in the Recommended Solution section to troubleshoot your problem."
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
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank.)",
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
            "required": true
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
            "id": "connection_pooler",
            "order": 5,
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
            "order": 6,
            "visibility": "connection_pooler == Yes",
            "controlType": "textbox",
            "displayLabel": "Which connection pooler are you using?",
            "required": false
        },
        {
            "id": "connection_pooler_config",
            "order": 7,
            "visibility": "connection_pooler == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Can you provide the connection pooling configuration?",
            "required": false
        },
        {
            "id": "workload",
            "order": 8,
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
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any driver exceptions or errors you received and any other information you want to share with us.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
