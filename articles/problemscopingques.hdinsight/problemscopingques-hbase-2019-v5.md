<properties
	articleId="8b5417d1-d7a0-42f0-8c59-d0b511f9a430"
	pageTitle="Scoping Questions for HDInsight HBase query Issue"
	description="Scoping Questions for HDInsight HBase Query Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636454, 32636452, 32636451"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HBase Query Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HBase Query Issue",
    "fileAttachmentHint": "Please attach YARN Application log, HBase Master log, HBase Region Server log, and Azure Storage debug log (if available) to help us triage your problem faster",
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
            "displayLabel": "Any change made?",
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
            "id": "load_increase",
            "order": 80,
            "controlType": "dropdown",
            "displayLabel": "Increase in load?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Numberjobs",
                    "text": "Number of jobs"
                },
                {
                    "value": "Moredata",
                    "text": "More data to be processed"
                },
                {
                    "value": "skew",
                    "text": "Increased skew in data to be processed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "application_id",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "YARN Application ID for the HBase job if known",
            "required": false
        },
        {
            "id": "hbase_query",
            "order": 200,
            "controlType": "multilinetextbox",
            "displayLabel": "HBase query",
            "watermarkText": "HBase query - please replace any parameter value containing PII information in your query",
            "required": false
        },
        {
            "id": "hbase_submission_method",
            "order": 300,
            "controlType": "dropdown",
            "displayLabel": "How was the HBase job submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HBase shell",
                    "text": "HBase shell"
                },
                {
                    "value": "Phoenix",
                    "text": "Phoenix"
                },
                {
                    "value": "REST API",
                    "text": "REST API"
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
            "watermarkText": "Please provide the detail symptom including the full error text, exception callstack if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
