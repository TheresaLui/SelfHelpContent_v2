<properties
	pageTitle="HDInsight Spark Issue"
	description="HDInsight Spark Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32511212,32511213,32511216,32511215"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Spark Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight Spark Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "spark_submission_method",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "How was the Spark Job submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Jupyter",
                    "text": "Jupyter"
                },
                {
                    "value": "Livy",
                    "text": "Livy"
                },
                {
                    "value": "Zeppelin",
                    "text": "Zeppelin"
                },
                {
                    "value": "Command Line",
                    "text": "Command Line"
                },
                {
                    "value": "ODBC/JDBC",
                    "text": "ODBC/JDBC"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "spark_programminglanguage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the programming language used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "Scala",
                    "text": "Scala"
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
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "YARN Application Id in case of job failure",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "YARN Application Id in case of job failure"
                }
            ]
        },
        {
            "id": "sparkconfig_details",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details.",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                },
                {
                    "text": "Spark executor and driver configuration including number of cores, memory etc."
                }
            ]
        },
        {
            "id": "learn_more_text",
            "order": 6,
            "controlType": "infoblock",
            "content": "<a href='https://hdinsight.github.io/spark/spark-landing'>Learn more</a> about commonly faced issues with using Spark on HDInsight"
        }
    ]
}
---
