<properties
	articleId="problemscopingques-netappvolume-developmentSDKissue"
	pageTitle="Issues using Development SDK"
	description="Issues using Development SDK"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740773,32740774"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues using Development SDK
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues using Development SDK",
    "fileAttachmentHint": "",
    "formElements": [
	{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
    	},
	{
            "id": "DEVtype",
	    "order": 2,
	    "controlType": "dropdown",
	    "displayLabel": "Issues with REST API, SDKs, CLI or ARM Templates?",
	    "watermarkText": "Select the type of development issue",
	    "dropdownOptions": [
	    	{
			"value": "devRESTAPI",
			"text": "Issue with REST API"
		},
	   	{
			"value": "devSDK",
			"text": "Issue with using SDKs"
		},
	     	{
			"value": "devCLI",
			"text": "Issues with using CLI"
	     	},
	     	{
			"value": "devARMtemplates",
			"text": "Issue with using ARM Templates"
	     	},
	     	{
			"value": "dont_know_answer",
			"text": "None of the above"
	      	}
	    ],
		"required": false
	},
	{
		"id": "RESTAPIused",
		"order": 3,
		"visibility": "DEVtype == devRESTAPI",
		"controlType": "multilinetextbox",
		"displayLabel": "What was the REST operation, resource type and version causing the issue?",
		"required": false
	},
	{
		"id": "ARMtemplateused",
		"order": 4,
		"visibility": "DEVtype == devARMtemplates",
		"controlType": "multilinetextbox",
		"displayLabel": "What ARM template is causing the issue?",
		"required": false
	},
	{
		"id": "SDKused",
		"order": 5,
		"visibility": "DEVtype == devSDK",
		"controlType": "dropdown",
		"displayLabel": "What type of SDK is causing the issue?",
		"watermarkText": "Select SDK causing the issue",
		"dropdownOptions": [
			{
				"value": "SDKforNET",
				"text": "SDK for .NET"
			},
			{
				"value": "SDKforPython",
				"text": "SDK for Python"
			},
			{
				"value": "SDKforGo",
				"text": "SDK for Go"
			},
			{
				"value": "SDKforJava",
				"text": "SDK for Java"
			},
			{
				"value": "SDKforJavaScript",
				"text": "SDK for JavaScript"
			},
			{
				"value": "SDKforRuby",
				"text": "SDK for Ruby"
			},
			{
				"value": "dont_know_answer",
				"text": "None of the above"
			}
		],
			"required": false
	},
	{
		"id": "CLIused",
		"order": 6,
		"visibility": "DEVtype == devCLI",
		"controlType": "dropdown",
		"displayLabel": "If using CLI, select CLI tool?",
		"watermarkText": "Select the CLI tool that is causing the issue",
		"dropdownOptions": [
			{
				"value": "AzureCLI",
				"text": "Azure CLI"
			},
			{
				"value": "PowerShell",
				"text": "PowerShell"
			},
			{
				"value": "dont_know_answer",
				"text": "None of the above"
			}
		],
			"required": false
	},
	{
            "id": "error_message",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
    	},
    	{
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide any other additional details",
            "required": true,
            "useAsAdditionalDetails": true
    	}
    ],
    "$schema": "SelfHelpContent"
}
---
