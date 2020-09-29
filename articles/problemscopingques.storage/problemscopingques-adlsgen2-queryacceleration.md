<properties
	pageTitle="Query Acceleration Issues with ADLS Gen2"
	description="Query Acceleration Issues with ADLS Gen2"
	authors="kartikshah9"
    ms.author="kashah"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32691202"
	productPesIds="16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="ea3e7267-f8e7-46ae-a0e7-4bbdb64717e5"
	ownershipId="StorageMediaEdge_DataLakeStorageGen2"
/>
# Query Acceleration Issues with ADLS Gen2
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Query Acceleration Issues with ADLS Gen2",
    "fileAttachmentHint": "",
    "formElements":
	[{
        "id": "problem_type",
        "order": 1,
        "controlType": "dropdown",
        "displayLabel": "How would you want us to help you?",
        "watermarkText": "Choose a problem area",
        "dropdownOptions": [{
            "value": "Issue",
            "text": "Troubleshoot a query issue"
        }, {
            "value": "Advisory",
            "text": "Need advisory guidance"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    },{
        "id": "problem_start_time",
        "order": 2,
        "visibility": "problem_type == Issue",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local start time of the most recent occurrence",
        "required": true
    }, {
        "id": "problem_end_time",
        "order": 3,
        "visibility": "problem_type == Issue",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local end time of the most recent occurrence. Enter current time if the performance issue is still continuing",
        "required": true
    },{
        "id": "problem_description",
        "order": 4,
        "controlType": "multilinetextbox",
        "displayLabel": "Provide details of your issue. For troubleshooting issues provide additional details like error message or exception stack",
        "required": true,
        "useAsAdditionalDetails": true
    }]
 }
---
