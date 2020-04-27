<properties
	articleId="4eac1b8b-2f38-4a86-b0f3-4c2e1df4a294"
	pageTitle="Scoping Questions for HDInsight Authentication with ODBC in standard cluster Issue"
	description="Scoping Questions for HDInsight Authentication with ODBC in standard cluster Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636487"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight Authentication with ODBC in standard cluster Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HDFS Authentication with ODBC in standard cluster Issue",
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
            "id": "connection_string",
            "order": 350,
            "controlType": "textbox",
            "displayLabel": "Connection string being used",
            "required": true
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
