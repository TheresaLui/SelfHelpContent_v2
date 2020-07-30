<properties
	pageTitle="CosmosDB Database Level Throughput"
	description="CosmosDB Database Level Throughput"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636786"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="ce1a9d62f-c4aa-43e6-849c-ea5c2b6cbf81"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Database Level Throughput
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Database Level Throughput",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "database_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
		{
            "id": "request_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you want to request an increase on the number of containers allowed in a shared throughput database?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
		{
            "id": "throughput_workloadtype",
            "order": 4,
			"visibility": "request_type == Yes",
            "controlType": "dropdown",
            "displayLabel": "What kind of workload are you using the shared throughput database for?",
			"watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Development",
                    "text": "Development"
                },
                {
                    "value": "Testing",
                    "text": "Testing"
                },
                {
                    "value": "QA",
                    "text": "QA"
                },
				{
                    "value": "Production",
                    "text": "Production"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "containers_count",
            "order": 5,
			"visibility": "request_type == Yes",
            "controlType": "textbox",
            "displayLabel": "How many containers do you plan to create in the shared throughput database?",
            "required": true
        },
		{
            "id": "acknowledge_impact",
            "order": 6,
			"visibility": "request_type == Yes",
            "controlType": "dropdown",
            "displayLabel": "I acknowledge and understand the impact of increasing the container limit on the overall throughput (RUs) distribution across the containers. For every set of 25 containers, the set will only be able to use up to a fraction of the overall RU/s provisioned on the database, as described in the previous article",
            "infoBalloonText": "Please read the section **Throughput distribution in database level offer** in the previous **Solutions** page or view in github https://aka.ms/cosmos-css-shared-db-doc",
			"watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---