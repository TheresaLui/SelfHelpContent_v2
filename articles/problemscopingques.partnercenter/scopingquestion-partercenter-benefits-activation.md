<properties
       pageTitle="Benefits activation issues"
       description="Benefits activation ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725862"
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_benefits_activation" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Benefits activation issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Benefits activation issues",
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
     "visibility": "benefit_activation == azure_cloud",
	   "controlType": "dropdown",
	   "displayLabel": "What is the help you are looking for?",
     "watermarkText":"Please select a category from the below list",
	   "dropdownOptions": [
	    {
	     "value": "Activated on incorrect tenant",
		   "text": "Activated on incorrect tenant"
	    },
	    {
		   "value": "Activation policy",
		   "text": "Activation policy"
	    },
	    {
		   "value": "Added seats instead of renew",
		   "text": "Added seats instead of renew"
	    },
	    {
		   "value": "Benefits swap",
		   "text": "Benefits swap"
	    },
	    {
		   "value": "Extending IURs",
		   "text": "Extending IURs"
	    },
	    {
		   "value": "How to activate",
		   "text": "How to activate"
	    },
	    {
		   "value": "Tokens not working or expired",
		   "text": "Tokens not working or expired"
	    },
	    {
       "value": "dont_know_answer",
       "text": "Not sure / Other"
	    }
	    ],
	 "required": false
    },
    {
	   "id": "onprem_software_details",
     "order": 4,
     "visibility": "benefit_activation == onprem_software",
	   "controlType": "dropdown",
	   "displayLabel": "What is the help you are looking for?",
     "watermarkText":"Please select a category from the below list",
	   "dropdownOptions": [
	    {
	     "value": "Additional activation request",
		   "text": "Additional activation request"
	    },
	    {
		   "value": "Discrepancies_questions on available licenses",
		   "text": "Discrepancies / Questions on available licenses"
	    },
	    {
		   "value": "Error activation the product keys",
		   "text": "Error activation the product keys"
	    },
	    {
		   "value": "Error downloading software",
		   "text": "Error downloading software"
	    },
	    {
		   "value": "How to download_activate",
		   "text": "How to download / activate"
	    },
	    {
		   "value": "Licenses statement or Usage policy",
		   "text": "Licenses statement / Usage policy"
	    },
	    {
		   "value": "Product key is not working",
		   "text": "Product key is not working"
	    },
	    {
		   "value": "User assignment",
		   "text": "User assignment"
	    },
	    {
       "value": "dont_know_answer",
       "text": "Not sure / Other"
	    }
	    ],
	 "required": false
    },
    {
	   "id": "visual_studio_details",
     "order": 5,
     "visibility": "benefit_activation == visual_studio",
	   "controlType": "dropdown",
	   "displayLabel": "What is the help you are looking for?",
     "watermarkText":"Please select a category from the below list",
	   "dropdownOptions": [
	    {
	     "value": "Additional activation request",
		   "text": "Additional activation request"
	    },
	    {
		   "value": "Discrepancies_questions on available licenses",
		   "text": "Discrepancies / Questions on available licenses"
	    },
	    {
		   "value": "Error activation the product keys",
		   "text": "Error activation the product keys"
	    },
	    {
		   "value": "Error downloading software",
		   "text": "Error downloading software"
	    },
	    {
		   "value": "How to download_activate",
		   "text": "How to download / activate"
	    },
	    {
		   "value": "Licenses statement or Usage policy",
		   "text": "Licenses statement / Usage policy"
	    },
	    {
		   "value": "Product key is not working",
		   "text": "Product key is not working"
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
	   "order": 6,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any additional information about the issue you've selected above",
     "infoBalloonText": "<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to use the Problem Steps Recorder in Microsoft 365</a>",
	   "required": true,
	   "useAsAdditionalDetails": true
    },
    {
	   "id": "problem_start_time",
	   "order": 7,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
    }
  ]
}
---
