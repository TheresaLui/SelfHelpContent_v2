<properties
       pageTitle="MPN enrollment issues"
       description="MPN enrollment issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728291"
       productPesIds="17000"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_mpn_enrollment_issues" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# MPN enrollment issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "MPN enrollment issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording, PSR or a document with steps to recreate the issue)",
   "formElements": [
   {
            "id": "mpn_benefit_program",
            "order": 1,
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
                    "value": "Gold",
                    "text": "Gold"
                },
                {
                    "value": "Silver",
                    "text": "Silver"
                },
		{
                    "value": "MAPS",
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
    "id": "what_help",
    "order": 2,
    "controlType": "dropdown",
    "displayLabel": "What is the help you are looking for?",
    "watermarkText": "Please select a help topic from the below list",
            "dropdownOptions": [
		{
                    "value": "account_creation_management",
                    "text": "MPN Account creation and management"
                },
                {
                    "value": "program_enrolment",
                    "text": "MPN program enrolment"
                },
                {
                    "value": "user_management",
                    "text": "User management"
                },
		{
		   "value": "dont_know_answer",
		   "text": "Not sure / Other"
	       }
            ],
    "infoBalloonText": "If you need help to create a net new account in Partner Center, please check the <a href='https://docs.microsoft.com/partner-center/mpn-create-a-partner-center-account'>Create a Partner Center account</a> webpage.",
    "required": true
    },
    {
     "id": "problem_description",
     "order": 3,
     "controlType": "multilinetextbox",
     "displayLabel": "Details",
     "watermarkText": "Please provide any additional information about your issue",
     "infoBalloonText": "To help us better understand your issue and for a faster resolution please upload the PSR (<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to take a PSR</a>)",
     "required": true,
     "useAsAdditionalDetails": true
     },
     {
      "id": "problem_start_time",
       "order": 4,
       "controlType": "datetimepicker",
       "displayLabel": "Start Date",
       "watermarkText": "When did your issue begin?",
       "required": true
      }
   ]
}
---
