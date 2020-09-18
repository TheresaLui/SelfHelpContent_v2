<properties
	pageTitle="Performance issue on table"
	description="Performance issue on table"
	authors="kartikshah9"
    	ms.author="kashah"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602885"
	productPesIds="16461"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="c3546c6d-ca17-4469-b00a-5a84d061d33d"
	ownershipId="StorageMediaEdge_StorageQueues"
/>
# Performance issue on table
---
{
	"$schema": "SelfHelpContent",
	"subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance issue on table scoping question",
    "fileAttachmentHint": "",
    "formElements":
	[
    {
        "id": "queue_names",
        "order": 1,
        "controlType": "multiselectdropdown",
        "displayLabel": "Queue Names",
        "watermarkText": "Select from your queues",
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/queueServices/default/queues?api-version=2019-06-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "name",
            "textPropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Not applicable/No queues available"
            }
        }
    },
    {
        "id": "problem_type",
        "order": 2,
        "controlType": "dropdown",
        "displayLabel": "How would you want us to help you?",
        "watermarkText": "Choose a problem area",
        "dropdownOptions": [{
            "value": "Issue",
            "text": "Troubleshoot a performance issue"
        }, {
            "value": "Advisory",
            "text": "Need advisory guidance to improve performance"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    },
	{
        "id": "issue_nature",
        "order": 3,
        "visibility": "problem_type == Issue",
        "controlType": "dropdown",
        "displayLabel": "Is it currently ongoing or happened in past and resolved?",
        "watermarkText": "Choose whether it's currently ongoing or happened in past and resolved",
        "dropdownOptions": [{
            "value": "Issue_Ongoing",
            "text": "Reporting an ongoing performance issue"
        }, {
            "value": "Issue_Resolved",
            "text": "Need root cause for a resolved performance issue"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    }, {
        "id": "problem_start_time",
        "order": 4,
        "visibility": "issue_nature == Issue_Ongoing || issue_nature == Issue_Resolved",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local start time of the most recent occurrence",
        "required": true
    }, {
        "id": "problem_end_time",
        "order": 5,
        "visibility": "issue_nature == Issue_Resolved",
        "controlType": "datetimepicker",
        "displayLabel": "Approximate local end time of the most recent occurrence. Enter current time if the performance issue is still continuing",
        "required": true
    }, {
        "id": "request_id",
        "order": 6,
        "visibility": "issue_nature == Issue_Ongoing || issue_nature == Issue_Resolved",
        "controlType": "textbox",
        "displayLabel": "Storage server Request ID",
        "watermarkText": "Request ID of failed operation ending with 000000",
        "textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
        "required": false
    }, {
        "id": "error_code_dropdown",
        "order": 7,
        "visibility": "issue_nature == Issue_Ongoing || issue_nature == Issue_Resolved",
        "controlType": "dropdown",
        "displayLabel": "Error code",
        "watermarkText": "HTTP error of failed operation",
        "dropdownOptions": [{
            "value": "HTTP_401",
            "text": "HTTP 401"
        }, {
            "value": "HTTP_403",
            "text": "HTTP 403"
        }, {
            "value": "HTTP_409",
            "text": "HTTP 409"
        }, {
            "value": "HTTP_500",
            "text": "HTTP 500"
        }, {
            "value": "HTTP_503",
            "text": "HTTP 503"
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
    },
	{
        "id": "table_name",
        "order": 8,
        "visibility": "issue_nature == Issue_Ongoing || issue_nature == Issue_Resolved",
        "controlType": "textbox",
        "displayLabel": "Queue URL path",
        "watermarkText": "Queue name or path",
        "required": false
    }, {
        "id": "problem_description",
        "order": 9,
        "controlType": "multilinetextbox",
        "displayLabel": "Provide details of your advisory ask. For troubleshooting issues provide additional details like error message or exception stack",
        "required": true,
        "useAsAdditionalDetails": true
    }
	]
 }
---
