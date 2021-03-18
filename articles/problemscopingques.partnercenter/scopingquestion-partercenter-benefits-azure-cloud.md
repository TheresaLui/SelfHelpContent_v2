<properties
       pageTitle="Azure and cloud benefits issues"
       description="Azure and cloud benefits ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32740047"
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_benefits_azure_cloud" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Azure and cloud benefits issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Azure and cloud benefits issues",
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
	 "id": "process_issue",
     "order": 2,
     "visibility": "true",
	 "controlType": "dropdown",
	 "displayLabel": "Please choose one of the below categories your issue is related with",
     "watermarkText":"Please select a category from the below list",
	 "dropdownOptions": [
	    {
	     "value": "azure_cloud_licenses",
		 "text": "Azure and Cloud licenses"
	    },
	    {
		 "value": "azure_credit",
		 "text": "Azure credit (Monthly / Bulk)"
	    },
	    {
		 "value": "dont_know_answer",
		 "text": "Not sure"
	    }
	    ],
	 "required": true
    },
    {
	 "id": "issue_details1",
     "order": 3,
     "visibility": "process_issue == azure_cloud_licenses",
	 "controlType": "dropdown",
	 "displayLabel": "What is your request related to?",
     "watermarkText":"Please select from the below list",
	 "dropdownOptions": [
        {
         "value": "activated_incorrect_tenant",
         "text": "Activated on incorrect tenant"
        },
        {
         "value": "seats_instead_renewing",
         "text": "Added seats instead of renewing"
        },
        {
         "value": "benefits_swap",
         "text": "Benefits swap"
        },
        {
         "value": "extension_iur_licenses",
         "text": "Extension of IUR licenses"
        },
        {
         "value": "how_to_activate",
         "text": "How to activate"
        },
        {
         "value": "questions_available_licenses",
         "text": "Questions on available licenses"
        },
        {
         "value": "questions_usage_policy",
         "text": "Questions on usage policy"
        },
        {
         "value": "tokens_notworking_expired",
         "text": "Tokens not working or expired"
        },
        {
         "value": "other_value",
         "text": "Other"
        }
    ],
     "required": false
    },
    {
	 "id": "issue_details2",
     "order": 4,
     "visibility": "process_issue == azure_credit",
	 "controlType": "dropdown",
	 "displayLabel": "Which type of credit you are having issues with?",
     "watermarkText":"Please select from the below list",
	 "dropdownOptions": [
	    {
		 "value": "monthly_azure_credit",
		 "text": "Monthly Azure credit"
	    },
	    {
		 "value": "bulk_azure_credit",
		 "text": "Bulk Azure Credit"
	    },
	    {
		 "value": "dont_know_answer",
		 "text": "Not sure"
	    }
	],
	 "required": true
    },
    {
	 "id": "issue_details3",
     "order": 5,
     "visibility": "process_issue == azure_credit",
	 "controlType": "dropdown",
	 "displayLabel": "What is the nature of your issue?",
     "watermarkText":"Please select from the below list",
	 "dropdownOptions": [
        {
         "value": "user_assignment",
         "text": "How do I assign a user"
        },
        {
         "value": "how_to_use",
         "text": "How to use bulk credits"
        },
        {
         "value": "user_assignment_issues",
         "text": "Issues while assigning the user"
        },
        {
         "value": "usage_policy_issues",
         "text": "Usage or Policy issues"
        },
        {
         "value": "other_value",
         "text": "Other"
        }
    ],
     "required": false
    },
    {
	 "id": "email_assigned",
	 "order": 6,
     "visibility": "process_issue == azure_credit",
	 "controlType": "textbox",
	 "displayLabel": "What is the user e-mail used to assign the above selected credit?",
	 "watermarkText": "Please provide the user e-mail used to assign the credit",
	 "required": true
    },
    {
	 "id": "product_name2",
	 "order": 7,
     "visibility": "process_issue == azure_cloud_licenses",
	 "controlType": "textbox",
	 "displayLabel": "What is the Product Name you have issues with?",
	 "watermarkText": "Please provide the Product Name",
	 "required": true
    },
    {
	 "id": "problem_description",
	 "order": 8,
	 "controlType": "multilinetextbox",
	 "displayLabel": "Details",
	 "watermarkText": "Please provide any additional information about the issue you've selected above",
     "infoBalloonText": "<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to use the Problem Steps Recorder in Microsoft 365</a>",
	 "required": true,
	 "useAsAdditionalDetails": true
    },
    {
	 "id": "problem_start_time",
	 "order": 9,
	 "controlType": "datetimepicker",
	 "displayLabel": "Start Date",
	 "watermarkText": "When did your issue begin?",
	 "required": true
    }
   ]
}
---
