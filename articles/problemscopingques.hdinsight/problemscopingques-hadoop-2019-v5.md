<properties
	articleId="ddf9f0c4-a747-423c-8f68-2d3c2e1942d1"
	pageTitle="Scoping Questions for HDInsight Hadoop Issue"
	description="Scoping Questions for HDInsight Hadoop Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636477, 32636476, 32636475"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# Hadoop Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight Hadoop MR Pig Sqoop Oozie Issue",
    "fileAttachmentHint": "Please attach YARN Application log, and client application output (if applicable) to help us triage your problem faster",
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
            "id": "problem_service",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Type of job that experienced the issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "MapReduce",
                    "text": "MapReduce"
                },
                {
                    "value": "Pig",
                    "text": "Pig"
                },
                {
                    "value": "Sqoop",
                    "text": "Sqoop"
                },
                {
                    "value": "Oozie",
                    "text": "Oozie"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "application_id",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "YARN Application ID for the job if known",
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
