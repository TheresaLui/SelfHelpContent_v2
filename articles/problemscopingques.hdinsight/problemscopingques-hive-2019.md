<properties
	articleId="7f30bed2-7dfa-4a20-8fe3-6d9d9f9cb22d"
	pageTitle="Scoping Questions for HDInsight Hive Issue"
	description="Scoping Questions for HDInsight Hive Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628993, 32629059, 32629060, 32629064, 32629065, 32629069, 32629094, 32629154, 32629057, 32629033, 32629163, 32629068, 32629062, 32629015"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Hive Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight Hive Issue",
    "fileAttachmentHint": "Please attach YARN Application log, HiveServer2 log to help us triage your problem faster",
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
            "id": "application_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "YARN Application ID for the Hive application",
            "required": true
        },
        {
            "id": "hive_query",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Hive query if applicable",
            "watermarkText": "Hive query",
            "required": true
        },
        {
            "id": "hive_query_plan",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Hive query explain plan if available",
            "watermarkText": "Hive query plan",
            "required": true
        },
        {
            "id": "hive_submission_method",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "How was the Hive query submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Beeline",
                    "text": "Beeline"
                },
                {
                    "value": "Ambari Hive View",
                    "text": "Ambari Hive view"
                },
                                {
                    "value": "ODBC",
                    "text": "ODBC"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide detailed symptoms, including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 8,
            "controlType": "infoblock",
            "content": "<a href='https://hdinsight.github.io/hive/hive-landing'>Learn more</a> about commonly faced issues with using Hive on HDInsight"
        }
    ]
}
---
