<properties
	pageTitle="HDInsight Kafka Issue"
	description="HDInsight Kafka Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32574298,32574299,32574302,32574304,32574305,32574306,32574309,32574311,32574314,32574315,32574318,32574320,32574321"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Kafka Issue
---
{
	"resourceRequired": true,
	"title": "HDInsight Kafka Issue",
	"fileAttachmentHint": "",
	"formElements": [
      {
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		  },{
			"id": "kafkaworkload_details",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details about the workload and the issue you are facing.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Number of topics and partitions per topic."
				}, {
					"text": "Number of producers and consumers."
				}, {
					"text": "Default replication factor."
				}, {
					"text": "Average number of messages per second and average message size."
				}
			]
		},{
			"id": "workloadmitigation_details",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Did you take any steps to mitigate the problem?",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "If so, describe the mitigation steps here."
				}
			]
		},{
			"id": "workloadcustomization_details",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Are there any third party tools/extensions deployed on the cluster?",
			"required": false,
			"useAsAdditionalDetails": false,
			"hints": [{
					"text": "If so, list the tools/extensions here."
				}
			]
		},{
			"id": "learn_more_text",
			"order": 5,
			"controlType": "infoblock",
			"content": "<a href='https://hdinsight.github.io/kafka/kafka-landing'>Learn more</a> about commonly faced issues with using Kafka on HDInsight"
		}
	]
}
---
