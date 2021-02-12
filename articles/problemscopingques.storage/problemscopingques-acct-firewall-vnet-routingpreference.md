<properties
	pageTitle="Storage account routing preference"
	description="Storage account routing preference"
	authors="annayak"
    ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742282"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques_acct_firewall_vnet_routingpreference"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Storage account routing preference
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue using storage account routing preference",
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
            "text": "I have some other issue"
        }],
        "required": true
    },
    {
        "id": "route_type",
        "order": 2,
        "controlType": "dropdown",
        "displayLabel": "Which routes are you having the issues with?",
        "watermarkText": "Choose the route type",
        "dropdownOptions": [{
            "value": "microsoft",
            "text": "Microsoft"
        }, {
            "value": "internet",
            "text": "Internet"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    },{
        "id": "issue_type",
        "order": 3,
        "controlType": "dropdown",
        "displayLabel": "What kind of issue are you facing with these routes?",
        "watermarkText": "Choose an issue area",
        "dropdownOptions": [{
            "value": "connectivity",
            "text": "Connectivity"
        }, {
            "value": "network",
            "text": "Network"
        },{
            "value": "latency_performance",
            "text": "Latency and Performance"
        },{
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    },
    {
        "id": "problem_start_time",
        "order": 4,
        "visibility": "problem_type == Issue",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local start time of the issue",
        "required": true
    }, {
        "id": "problem_end_time",
        "order": 5,
        "visibility": "problem_type == Issue",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local end time of the issue",
        "required": true
    },{
        "id": "problem_description",
        "order": 6,
        "controlType": "multilinetextbox",
        "displayLabel": "Provide details of your issue. For troubleshooting issues provide additional details like error message or exception stack",
        "required": true,
        "useAsAdditionalDetails": true
    }]
 }
---
