<properties
  pageTitle="Scaling Based on Schedule or Workload"
	description="Scaling Based on Schedule or Workload"
	authors="Johirsch"
	ms.author="Johirsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630452"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-scaling-based-on-schedule-or-workload"
/>

# Scaling Based on Schedule or Workload
---
{
	"resourceRequired": true,
	"title": "Scaling Based on Schedule or Workload",
	"fileAttachmentHint": "",
	"subscriptionRequired": true,
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
