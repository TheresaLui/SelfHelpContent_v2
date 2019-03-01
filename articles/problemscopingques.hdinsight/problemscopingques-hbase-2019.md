<properties
	articleId="5a20bbc6-9892-4520-8876-b23c1ebd4fe0"
	pageTitle="Scoping Questions for HDInsight HBase Issue"
	description="Scoping Questions for HDInsight HBase Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628992, 32629045, 32629046, 32629049, 32629050, 32629053"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# HBase Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight HBase Issue",
    "fileAttachmentHint": "Please attach YARN Application log, HBase Master log, HBase Region Server log (if applicable), and Azure Storage debug log (if available) to help us triage your problem faster",
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
            "displayLabel": "YARN Application ID for the HBase application",
            "required": true
        },
        {
            "id": "hbase_submission_method",
            "order": 4,
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
                    "value": "Other (describe below)",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "hbase_query",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "HBase query",
            "watermarkText": "HBase query - please replace any parameter value containing PII information in your query",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text (if available), whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 8,
            "controlType": "infoblock",
            "content": "<a href='https://hdinsight.github.io/hbase/hbase-landing'>Learn more</a> about commonly faced issues with using Spark on HDInsight"
        }
    ]
}
---
