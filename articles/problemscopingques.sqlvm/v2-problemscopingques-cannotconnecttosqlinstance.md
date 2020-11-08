<properties 
  pageTitle="Cannot connect to SQL Instance"
  description="Cannot connect to SQL Instance"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740109"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="7c42fe8d-ed95-4b4c-952a-bdcb693dd2d8"
 ownershipId="AzureData_AzureSQLVM"
/>
# Cannot connect to SQL Instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Cannot connect to SQL Instance",
	"fileAttachmentHint": "",
	"diagnosticCard": {
    "title": "Cannot connect to SQL Instance Troubleshooter",
    "description": "Cannot connect to SQL Instance Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true,
            "diagnosticInputRequiredClients": "Portal"
	    },{
            "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes your Cannot connect to SQL Instance issue.",
            "watermarkText": "Common Cannot connect to SQL Instance categories",
            "infoBalloonText": "Cannot connect to SQL Instance issue category",
            "dropdownOptions": [
            {
            "value": "CannotConnectToSQLInstance",
            "text": "Cannot Connect to SQL instance"
            },

            {
            "value": "AvailabilityGroupsConfiguration_SetupListenerAndLoadBalancer",
            "text": "Setup Listener and Load Balancer for Availability Groups"
            },
            {
            "value": "AvailabilityGroupsConfiguration_Listener_ConnectivityIssue",
            "text": "Configured Availability Group but Unable to connect using Listener."
            },

            {
            "value": "dont_know_answer",
            "text": "None of the above"
            }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        }, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Name of the virtual machine(s) in the same subscription that you think is faster than the slow virtual machine."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://jsonlint.com/'>Use this JSON Checker</a> if you are receiving validation errors in your scoping question"
		}
	]
}
---
