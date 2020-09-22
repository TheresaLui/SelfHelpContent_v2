<properties
	articleId="09ebd4c4-b0a8-41b2-8790-5536b3b463c2"
	pageTitle="Scoping Questions for HDInsight Authentication with Notebook in standard cluster Issue"
	description="Scoping Questions for HDInsight Authentication with Notebook in standard cluster Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636483"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight Authentication with Notebook in standard cluster Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HDFS Authentication with Notebook in standard cluster Issue",
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
            "id": "user_scope",
            "order": 200,
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
