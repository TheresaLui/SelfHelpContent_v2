<properties
	articleId="0eba545f-b093-4a87-9d02-14055791dbe2"
	pageTitle="Scoping Questions for HDInsight Authentication with ODBC in ESP Issue"
	description="Scoping Questions for HDInsight Authentication with ODBC in ESP Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636486"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight Authentication with ODBC in ESP Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HDFS Authentication with ODBC in ESP Issue",
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
            "id": "connection_string",
            "order": 30,
            "controlType": "textbox",
            "displayLabel": "Connection string being used",
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
            "required": true
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
            "required": true
        },
        {
            "id": "hdfs-ls-work",
            "order": 310,
            "controlType": "dropdown",
            "displayLabel": "Does hdfs dfs -ls / work?",
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
            "id": "hdfs-error",
            "order": 320,
            "visibility": "hdfs-ls-work == No",
            "controlType": "textbox",
            "displayLabel": "hdfs dfs -ls error message",
            "required": false
        },
        {
            "id": "beeline",
            "order": 400,
            "controlType": "dropdown",
            "displayLabel": "Does Beeline work from within the cluster using zookeeper connection string copied from Ambari?",
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
            "id": "beeline_connection_string",
            "order": 450,
            "visibility": "beeline == Yes",
            "controlType": "textbox",
            "displayLabel": "Connection string used from Beeline",
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
