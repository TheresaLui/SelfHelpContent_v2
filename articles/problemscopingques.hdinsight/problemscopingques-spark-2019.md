<properties
	articleId="7ac8675e-cb6f-43b4-8684-8f794ac5034f"
	pageTitle="Scoping Questions for HDInsight Spark Issue"
	description="Scoping Questions for HDInsight Spark Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629134, 32629136, 32628998, 32629061, 32629075, 32629079, 32629081, 32629093, 32629133, 32629135, 32629137, 32629138, 32629139, 32629140, 32629141, 32629142, 32629143, 32629144, 32629166"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Spark Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight Spark Issue",
    "fileAttachmentHint": "Please attach YARN Application log, Spark log, and Spark-submit output (if applicable) to help us triage your problem faster",
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
            "displayLabel": "YARN Application ID for the Spark application",
            "required": true
        },
        {
            "id": "spark_submission_method",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "How was the Spark job submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Jupyter",
                    "text": "Jupyter Notebook"
                },
                {
                    "value": "Zeppelin",
                    "text": "Zeppelin Notebook"
                },
                {
                    "value": "Livy",
                    "text": "Livy"
                },
                {
                    "value": "Spark shell",
                    "text": "Spark shell"
                },
                {
                    "value": "ADF",
                    "text": "Azure Data Factory"
                },
                {
                    "value": "ODBC/JDBC",
                    "text": "ODBC/JDBC"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "spark_programminglanguage",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the programming language used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Scala",
                    "text": "Scala"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "R",
                    "text": "R"
                },
                {
                    "value": "Java",
                    "text": "Java"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (mention below in the description)"
                }
            ],
            "required": true
        },
        {
            "id": "sparkconfig_details",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Spark configuration details",
            "watermarkText": "Complete Spark-submit command, or config info on number of executors, executor cores, and executor memory",
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
            "content": "<a href='https://hdinsight.github.io/spark/spark-landing'>Learn more</a> about commonly faced issues with using Spark on HDInsight"
        }
    ]
}
---
