<properties
	pageTitle="HDInsight Storm Issue"
	description="HDInsight Storm Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32511221,32511222,32511223,32511224"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Kafka Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight Storm Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details about the topology and the issue you are facing.",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                },
                {
                    "text": "Name of the affected topology."
                },
                {
                    "text": "Number of spouts and bolts."
                },
                {
                    "text": "Parallelism for spouts and bolts."
                }
            ]
        },
        {
            "id": "workloadmitigation_details",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Did you take any steps to mitigate the problem?",
            "required": false,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "If so, describe the mitigation steps here."
                }
            ]
        },
        {
            "id": "workloadcustomization_details",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Are there any third party tools/extensions deployed on the cluster?",
            "required": false,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "If so, list the tools/extensions here."
                }
            ]
        },
        {
            "id": "learn_more_text",
            "order": 5,
            "controlType": "infoblock",
            "content": "<a href='https://hdinsight.github.io/storm/storm-landing'>Learn more</a> about commonly faced issues with using Storm on HDInsight"
        }
    ]
}
---
