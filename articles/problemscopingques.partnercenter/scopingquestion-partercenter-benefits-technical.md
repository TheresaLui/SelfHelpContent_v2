<properties
       pageTitle="Benefits - Technical benefits issues"
       description="Benefits - Technical benefits ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32740051"
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_benefits_technical" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Benefits - Technical benefits issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Benefits - Technical benefits issues",
   "fileAttachmentHint": "Please upload supporting files that can help us better understand your issue (screen recording or document with steps to recreate the issue)",
   "formElements": [
    {
     "id": "mpn_benefit_program",
     "order": 1,
     "visibility": "true",
     "controlType": "dropdown",
     "displayLabel": "What offer or program are you having issues with?",
     "watermarkText": "Select an offer/program type",
     "dropdownOptions": [
      {
       "value": "advanced_spec",
       "text": "Advanced Specialization"
      },
      {
       "value": "azure_exp_msp",
       "text": "Azure Expert MSP"
      },
      {
       "value": "gold_value",
       "text": "Gold"
      },
      {
       "value": "silver_value",
       "text": "Silver"
      },
      {
       "value": "maps_value",
       "text": "MAPS"
      },
      {
       "value": "dont_know_answer",
       "text": "Not sure / Other"
      }
    ],
     "required": true
    },
    {
	 "id": "support_type",
     "order": 2,
     "visibility": "true",
	 "controlType": "dropdown",
	 "displayLabel": "What is the technical benefit support that you are looking for",
     "watermarkText":"Please select a category from the below list",
	 "dropdownOptions": [
	    {
	     "value": "product_support",
		 "text": "Looking for a product support"
	    },
	    {
		 "value": "consultation_support",
		 "text": "Looking for consultation support with pre-sales / deployment"
	    },
	    {
         "value": "dont_know_answer",
         "text": "Not sure / Other"
	    }
	    ],
	   "required": true
    },
    {
	 "id": "product_support_details",
     "order": 3,
     "visibility": "support_type == product_support",
	 "controlType": "dropdown",
	 "displayLabel": "What is the help you are looking for?",
     "watermarkText":"Please select a category from the below list",
	 "dropdownOptions": [
	    {
	     "value": "accessid_contractid",
		 "text": "Access ID / contract ID"
	    },
	    {
		 "value": "activating_incident",
		 "text": "Activating incident"
	    },
	    {
		 "value": "incident_inquiries",
		 "text": "Product support incident inquiries"
	    },
	    {
         "value": "dont_know_answer",
         "text": "Not sure / Other"
	    }
	    ],
	 "required": false
    },
    {
	 "id": "consultation_support_details",
     "order": 4,
     "visibility": "support_type == consultation_support",
	 "controlType": "dropdown",
	 "displayLabel": "What is the help you are looking for?",
     "watermarkText":"Please select a category from the below list",
	 "dropdownOptions": [
	    {
	     "value": "advisory_hours",
		 "text": "Partner advisory hours"
	    },
	    {
         "value": "dont_know_answer",
         "text": "Not sure / Other"
	    }
	    ],
	 "required": false
    },
    {
	 "id": "problem_description",
	 "order": 5,
	 "controlType": "multilinetextbox",
	 "displayLabel": "Details",
	 "watermarkText": "Please provide any additional information about the issue you've selected above",
     "infoBalloonText": "<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to use the Problem Steps Recorder in Microsoft 365</a>",
	 "required": true,
	 "useAsAdditionalDetails": true
    },
    {
	 "id": "problem_start_time",
	 "order": 6,
	 "controlType": "datetimepicker",
	 "displayLabel": "Start Date",
	 "watermarkText": "When did your issue begin?",
	 "required": true
    }
  ]
}
---
