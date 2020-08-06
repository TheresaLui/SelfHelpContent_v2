<properties
  pageTitle="Scaling Based on Schedule or Workload"
	description="Scaling Based on Schedule or Workload"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630452"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="D3FA08A1-5FF6-4FCC-B7D9-94C7AE055296"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# Scaling Based on Schedule or Workload
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "Scaling Based on Schedule or Workload",
	"fileAttachmentHint": "",
	"subscriptionRequired": false,
	"formElements": [
	    {
		      "id": "query_or_operation",
			    "order": 1,
			    "controlType": "multilinetextbox",
    			"displayLabel": "If you were trying to run a query or operation, please provide it.",
		    	"required": false,
			    "visibility": true
	    },
	  	{
		  	"id": "problem_description",
			  "order": 2,
			  "controltype": "multilinetextbox",
			  "displayLabel": "Any additional details you would like to include?",
			  "watermarkText": "Enter any additional details here",
			  "infoBalloonText": "Enter any additional details here",
			  "required": true,
			  "useAsAdditionalDetails": true
		  },
		  {
			  "id": "problem_start_time",
			  "order": 3,
			  "controltype": "datetimepicker",
			  "displayLabel": "When did the problem begin?",
			  "watermarkText": "Specify when the problem started",
			  "infoBalloonText": "Specify when the problem started",
			  "required": true,
			  "useAsAdditionalDetails": false
		  }
	]
}
---
