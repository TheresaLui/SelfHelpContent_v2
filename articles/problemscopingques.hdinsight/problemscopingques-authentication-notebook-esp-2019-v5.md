<properties
	articleId="cfba0351-a65c-4766-a94f-a9b682152914"
	pageTitle="Scoping Questions for HDInsight Authentication with Notebook in ESP Issue"
	description="Scoping Questions for HDInsight Authentication with Notebook in ESP Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636482"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight Authentication with Notebook in ESP Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HDFS Authentication with Notebook in ESP Issue",
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
            "id": "notebook",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Type of Notebook?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Jupyter",
                    "text": "Jupyter"
                },
                {
                    "value": "Zeppelin",
                    "text": "Zeppelin"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "user_scope",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Does the issue affect all users or a few users?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "All_users",
                    "text": "All users"
                },
                {
                    "value": "Few_users",
                    "text": "A few users"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "ambari_login",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Does Ambari login work?",
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
            "id": "kinit",
            "order": 300,
            "controlType": "dropdown",
            "displayLabel": "Does kinit for some or all users work from the Head node?",
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
            "id": "clusteradmin",
            "order": 400,
            "controlType": "dropdown",
            "displayLabel": "Does authentication fail even for the cluster admin account?",
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
