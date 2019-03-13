<properties
	articleId="21b5b627-e2bf-49b5-9e31-f69f51a3cc18"
	pageTitle="Scoping Questions for HDInsight Kafka Broker Issue"
	description="Scoping Questions for HDInsight Kafka Broker Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628995, 32629018, 32629019, 32629020, 32629021, 32629074"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Kafka Broker Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight Kafka Issue",
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
            "id": "is_new_problem",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this a new problem, or it has happened before?",
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
                }
            ],
            "required": true
        },
        {
			"id": "previous_solution",
			"visibility": "is_new_problem == Happened_before",
			"order": 110,
			"controlType": "multilinetextbox",
            "displayLabel": "Previous solution if applicable",
            "watermarkText": "If the previous occurance was resolved, please share how it was resolved",
            "required": true
		},
        {
			"id": "change_made",
			"visibility": "is_new_problem == New_problem",
			"order": 120,
			"controlType": "multilinetextbox",
            "displayLabel": "Any changes made?",
            "watermarkText": "Any changes since last time it worked",
            "required": true
		},
        {
            "id": "number_total_brokers",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Total number of brokers on your Kafka cluster",
            "required": true
        },
        {
            "id": "number_problem_brokers",
            "order": 160,
            "controlType": "textbox",
            "displayLabel": "Number of brokers experienced the problem",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 600,
            "controlType": "infoblock",
            "content": "<a href='https://hdinsight.github.io/kafka/kafka-landing'>Learn more</a> about commonly faced issues with using Spark on HDInsight"
        }
    ]
}
---
