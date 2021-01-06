<properties
       pageTitle="Internal use rights IUR licenses issues"
       description="Internal use rights IUR licenses issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725871"
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_iur_issue"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Internal use rights IUR licenses issues issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Internal use rights IUR licenses issues issues",
   "fileAttachmentHint": "Please upload supporting files that can help us better understand your issue (screen recording or document with steps to recreate the issue)",
   "formElements": [
   {
    "id": "learn_more_text",
    "order": 1,
    "visibility": "true",
    "controlType": "infoblock",
    "content": "All licenses and products coming from MPN program have Internal Use Rights, meaning they should only be used for internal purposes only. See sections 'Product Licenses granted can be used for' and 'Product Licenses granted cannot be used for' in the <a href='https://assetsprod.microsoft.com/MPN-MAPS-Product-Usage-Guide.pdf'>Microsoft Partner Network benefits usage guide</a>."
   },
   {
     "id": "mpn_benefit_program",
     "order": 2,
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
     "id": "mpn_benefit_type",
     "order": 3,
     "visibility": "true",
     "controlType": "dropdown",
     "displayLabel": "What type of benefit are you having problem with?",
     "watermarkText": "Select benefit type",
     "dropdownOptions": [
      {
       "value": "azure_cloud_products",
       "text": "Azure and Cloud products"
      },
      {
       "value": "Software_products",
       "text": "Software products"
      },
      {
       "value": "visual_studio_subs",
       "text": "Visual studio subscriptions"
      },
      {
       "value": "dont_know_answer",
       "text": "Not sure / Other"
      }
      ],
     "required": true
    },
    {
	   "id": "issue_details",
	   "order": 4,
     "visibility": "mpn_benefit_type == azure_cloud_products",
	   "controlType": "dropdown",
	   "displayLabel": "What is the help you are looking for?",
	   "watermarkText": "Please select from the list below",
     "dropdownOptions": [
      {
       "value": "activated_incorrect_tenant",
       "text": "Activated on incorrect tenant"
      },
      {
       "value": "activation_issues",
       "text": "Activation issues or how to activate"
      },
      {
       "value": "seats_instead_renewing",
       "text": "Added seats instead of renewing"
      },
      {
       "value": "azure_bulk_credits",
       "text": "Azure bulk credits"
      },
      {
       "value": "azure_monthly_credits",
       "text": "Azure monthly credits"
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
       "value": "assignments_azure_credits",
       "text": "User assignments on azure credits"
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
	   "watermarkText": "Please provide any additional information about the issue that you've selected above",
     "infoBalloonText": "<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to use the Problem Steps Recorder in Microsoft 365</a>",
	   "required": true,
	   "useAsAdditionalDetails": true
    },
    {
	   "id": "problem_start_time",
	   "order": 6,
     "visibility": "true",
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
    }
   ]
}
---
