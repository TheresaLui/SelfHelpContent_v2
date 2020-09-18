<properties
	pageTitle="Issue using soft delete for Azure file share"
	description="Issue using soft delete for Azure file share"
	authors="kartikshah9"
    ms.author="kashah"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32736814"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="7a4d5978-e9dd-4a24-9dee-0a098e2d7023"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Issue using soft delete for Azure file share
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue using soft delete for Azure file share",
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
            "text": "Troubleshoot an issue"
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
        "displayLabel": "Approximate local start time of the issue",
        "required": true
    }, {
        "id": "problem_end_time",
        "order": 3,
        "visibility": "problem_type == Issue",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local end time of the issue",
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
