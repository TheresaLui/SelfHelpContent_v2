<properties
	pageTitle="HDInsight Spark Issue"
	description="HDInsight Spark Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32511173"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# VM Performance
---
{
	"resourceRequired": true,
	"title": "HDInsight Spark Issue",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "spark_submission_method",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "How was the Spark Job submitted?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Jupyter",
					"text": "Jupyter"
				}, {
					"value": "Livy",
					"text": "Livy"
				}, {
					"value": "Zeppelin",
					"text": "Zeppelin"
				},{
					"value": "Command Line",
					"text": "Command Line"
				},{
					"value": "ODBC/JDBC",
					"text": "ODBC/JDBC"
				},{
					"value": "Other (describe below)",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "spark_programminglanguage",
			"order": 3,
			"controlType": "multiselectdropdown",
			"displayLabel": "What is the programming language used?",
			"dropdownOptions": [{
					"value": "Python",
					"text": "Python"
				},{
					"value": "Scala",
					"text": "Scala"
				},{
					"value": "Other (describe below)",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "executor_driver_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide details about executor and driver configuration",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Number of cores, memory etc."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 5,
			"controlType": "infoblock",
			"content": "<a href='https://hdinsight.github.io/spark/spark-landing'>Learn more</a> about commonly faced issues with using Spark on HDInsight"
		}
	]
}
---
