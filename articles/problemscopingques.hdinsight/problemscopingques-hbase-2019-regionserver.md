<properties
	articleId="6bde26ec-032c-4cab-8122-03f5992e64bd"
	pageTitle="Scoping Questions for HDInsight HBase Region Server Issue"
	description="Scoping Questions for HDInsight HBase Region Server Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629051"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# HBase Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight HBase Issue",
    "fileAttachmentHint": "Please attach YARN Application log, HBase Region Server logs, and/or Azure Storage debug log (if available) to help us triage your problem faster",
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
            "id": "number_region_servers_impacted",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Number of region servers impacted",
            "required": true
        },
        {
            "id": "region_server_list",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Name of the region servers impacted (seperate with commas)",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information",
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
