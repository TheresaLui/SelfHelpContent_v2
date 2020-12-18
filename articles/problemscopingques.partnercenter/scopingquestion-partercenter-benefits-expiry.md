<properties
       pageTitle="Benefits expiry issues"
       description="Benefits expiry ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725863"
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_benefits_expiry"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Benefits expiry issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Benefits expiry issues",
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
	 "id": "benefit_activation",
     "order": 2,
     "visibility": "true",
	 "controlType": "dropdown",
	 "displayLabel": "Please choose one of the below categories your issue is related with",
     "watermarkText":"Please select a category from the below list",
	 "dropdownOptions": [
	    {
	     "value": "azure_cloud",
		 "text": "Azure and Cloud"
	    },
	    {
		 "value": "onprem_software",
		 "text": "On-prem Software"
	    },
	    {
		 "value": "visual_studio",
		 "text": "Visual Studio"
	    },
	    {
         "value": "dont_know_answer",
         "text": "Not sure / Other"
	    }
	    ],
	 "required": true
    },
    {
	 "id": "azure_cloud_details",
     "order": 3,
     "visibility": "true",
	 "controlType": "dropdown",
	 "displayLabel": "What is the help you are looking for?",
     "watermarkText":"Please select a category from the below list",
	 "dropdownOptions": [
	    {
	     "value": "benefits_dont_align",
		 "text": "Benefits dates don't align with the membership dates"
	    },
	    {
		 "value": "pmc_vs_partner_center",
		 "text": "Benefits expiry on PMC vs. Partner Center"
	    },
	    {
		 "value": "keys_tokens_expired",
		 "text": "Product keys or tokens have expired"
	    },
	    {
		 "value": "keys_tokens_not_working",
		 "text": "Product keys or tokens not working"
	    },
	    {
         "value": "dont_know_answer",
         "text": "Not sure / Other"
	    }
	    ],
	 "required": true
    },
    {
	 "id": "problem_description",
	 "order": 4,
	 "controlType": "multilinetextbox",
	 "displayLabel": "Details",
	 "watermarkText": "Please provide any additional information about the issue you've selected above",
     "infoBalloonText": "<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to use the Problem Steps Recorder in Microsoft 365</a>",
	 "required": true,
	 "useAsAdditionalDetails": true
    },
    {
	 "id": "problem_start_time",
	 "order": 5,
	 "controlType": "datetimepicker",
	 "displayLabel": "Start Date",
	 "watermarkText": "When did your issue begin?",
	 "required": true
    }
    ]
}
---
