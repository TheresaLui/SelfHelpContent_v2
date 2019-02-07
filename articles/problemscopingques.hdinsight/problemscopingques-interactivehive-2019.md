<properties
	articleId="dcab6070-482a-4e94-a3c4-e7ecb0a1f444"
	pageTitle="Scoping Questions for HDInsight Interactive Query Issue"
	description="Scoping Questions for HDInsight Interactive Query Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628994, 32629012, 32629014, 32629042, 32629063, 32629072, 32629078, 32629092, 32629104, 32629109, 32629164"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Ineractive Query Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight Interactive Query Issue",
    "fileAttachmentHint": "Please attach YARN Application log, HiveServer2Interactive log, and note any configuration setting that has been changed to help us triage your problem faster",
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
            "displayLabel": "YARN Application ID for the application",
            "required": true
        },
        {
            "id": "interactive_query",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Interactive query if applicable",
            "watermarkText": "Interactive query, please replace any PII parameter value in the query when needed",
            "required": true
        },
        {
            "id": "interactive_query_plan",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Interactive query plan if available",
            "watermarkText": "Interactive query plan",
            "required": true
        },
        {
            "id": "interactive_query_submission_method",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "How was the interactive query submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Beeline",
                    "text": "Beeline"
                },
                {
                    "value": "Zeppelin",
                    "text": "Zeppelin"
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
        }
    ]
}
---
