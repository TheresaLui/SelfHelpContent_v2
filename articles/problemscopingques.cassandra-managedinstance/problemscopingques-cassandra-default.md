<properties
	pageTitle="Cassandra Managed Instance Default scoping questions"
	description="Cassandra Managed Instance Default scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32788352,32788354,32788355,32788356,32788357,32788358,32788359,32788360,32788361,32788362,32788363,32788364,32788365,32788366,32788367,32788368"
    productPesIds="17480"
	cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="14340e43-7f28-49ed-b3e7-d1cc1a144763"
	ownershipId="AzureData_AzureManagedInstanceCassandra"
/>
# Cassandra Managed Instance Info
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cassandra Managed Instance Info",
    "fileAttachmentHint": "Please attach full exception stack.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "datacenter_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Data center name",
            "required": false
        },
        {
            "id": "clientdriver_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Client driver name",
            "required": false
        },
        {
            "id": "clientdriver_version",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Client driver version",
            "required": false
        },
        {
            "id": "cluster_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Which Cluster configuration are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Hybrid Cluster",
                    "text": "Hybrid Cluster"
                },
                {
                    "value": "Cassandra Cluster",
                    "text": "Cassandra Cluster"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "exception_message",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the exception message?",
            "required": false
        },
        {
            "id": "curl_command",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Curl command output for connectivity",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you experienced",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
