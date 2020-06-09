<properties
	articleId="74ef1615-59c3-412f-a468-eaf0bc0b4226"
	pageTitle="Scoping Questions for HDInsight Tez View Issue"
	description="Scoping Questions for HDInsight Tez View Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636505"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# Tez View Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight Tez View Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "is_new_problem",
            "order": 10,
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
            "required": true
        },
        {
            "id": "previous_solution",
            "visibility": "is_new_problem == Happened_before",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Previous solution if applicable",
            "watermarkText": "If the previous occurance was resolved, please share how it was resolved",
            "required": false
        },
        {
            "id": "changes_category",
            "visibility": "is_new_problem == New_problem",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Any change made to any of these components?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HDInsight_cluster",
                    "text": "HDInsight cluster configuration"
                },
                {
                    "value": "reboot",
                    "text": "Node or service reboot"
                },
                {
                    "value": "Network",
                    "text": "Network"
                },
                {
                    "value": "Storage_account",
                    "text": "Storage account"
                },
                {
                    "value": "access",
                    "text": "Password, access key, or certificate rotation"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "changes_detail",
            "visibility": "changes_category != dont_know_answer",
            "order": 50,
            "controlType": "multilinetextbox",
            "displayLabel": "Detail of the changes",
            "watermarkText": "Please describe the changes in detail",
            "required": false
        },
        {
            "id": "viewloaded",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "Did the view load?",
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
            "id": "intermittent",
            "order": 300,
            "controlType": "dropdown",
            "displayLabel": "Is the issue intermittent?",
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
            "id": "tardyresponse",
            "order": 400,
            "controlType": "dropdown",
            "displayLabel": "Is the issue regarding to tardy response?",
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
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, exception callstack if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
