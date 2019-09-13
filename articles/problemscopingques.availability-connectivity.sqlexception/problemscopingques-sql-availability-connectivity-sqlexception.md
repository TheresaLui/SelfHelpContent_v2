<properties
  pageTitle="SqlException received on the customer's client"
	description="SqlException received on the customer's client"
	authors="swbhartims"
	ms.author="swbhartims"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630429"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-sql-availability-connectivity-sqlexception"
/>

# SqlException received on the customer's client
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"title": "SqlException received on the customer's client",
	"fileAttachmentHint": "",
	"subscriptionRequired": false,
	"formElements": [
	    {
		      "id": "sqlexception_received_on_client",
			    "order": 1,
			    "controlType": "multilinetextbox",
    			"displayLabel": "Please provide the verbatim for the SQL error, or client error message you're seeing. Complete callstack (with appropriate user and/or application sensitive information redacted) is preferred.",
		    	"required": true,
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