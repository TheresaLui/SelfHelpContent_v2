<properties
	articleId="53bc517d-d719-4725-ad5f-709281c0d534"
	pageTitle="Scoping Questions for HDInsight Create Issue related to ADLS Gen2"
	description="Scoping Questions for HDInsight Create Issue related to ADLS Gen2"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636439"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDI Cluster Create Issue related to ADLS Gen2
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "HDInsight CRUD Issue",
    "fileAttachmentHint": "Please provide the ARM template and the exact command used for the CRUD operation, if applicable",
        "diagnosticCard": {
        "title": "HDInsight CRUD Troubleshooter",
        "description": "HDInsight CRUD Troubleshooter can help you troubleshoot and solve your CRUD problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "cluster_name",
            "order": 10,
            "controlType": "textbox",
            "displayLabel": "Cluster name",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "is_new_problem",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Is this a new problem, or the problem has happened before?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "New_problem",
                    "text": "New problem, worked before"
                },
                {
                    "value": "Never_worked",
                    "text": "Never worked"
                },
                {
                    "value": "Happened_before",
                    "text": "Not new, happened before"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "previous_solution",
            "visibility": "is_new_problem == Happened_before",
            "order": 110,
            "controlType": "multilinetextbox",
            "displayLabel": "Previous solution if applicable",
            "watermarkText": "If the previous occurance was resolved, please share how it was resolved",
            "required": false
        },
        {
            "id": "change_made",
            "visibility": "is_new_problem == New_problem",
            "order": 120,
            "controlType": "multilinetextbox",
            "displayLabel": "Any changes made?",
            "watermarkText": "Any changes since last time it worked",
            "required": false
        },
        {
            "id": "is_vnet_involved",
            "order": 140,
            "controlType": "dropdown",
            "displayLabel": "Is cluster created in a VNET?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "is_vnet_peering",
            "visibility": "is_vnet_involved == Yes",
            "order": 150,
            "controlType": "dropdown",
            "displayLabel": "Is VNET peering involved?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "is_aad_involved",
            "order": 180,
            "controlType": "dropdown",
            "displayLabel": "Is Azure Active Directory Domain Services Integration involved?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "CRUD_request_submission_method",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "How was the CRUD request submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "ARM Template",
                    "text": "ARM Template"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "Power Shell",
                    "text": "Power Shell"
                },
                {
                    "value": "Azure Data Factory Activity",
                    "text": "Azure Data Factory Activity"
                },
                {
                    "value": "Azure Automation runbook",
                    "text": "Azure Automation runbook"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---