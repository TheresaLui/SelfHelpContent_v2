<properties
       pageTitle="MPN enrollment issues"
       description="MPN enrollment issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds=""
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
       "id": "achieve_box",
       "order": 1,
	    "controlType": "textbox",
	    "displayLabel": "What are you trying to achieve?",
       "infoBalloonText": "If you need help to create a net new account in Partner Center, please check the <a href='https://docs.microsoft.com/partner-center/mpn-create-a-partner-center-account'>Create a Partner Center account</a> webpage. In case the issue persists please complete this ticket submission.",
	    "required": true
	   },
      {
       "id": "problem_description",
       "order": 2,
       "controlType": "multilinetextbox",
       "displayLabel": "Details",
       "watermarkText": "Please provide any additional information about your issue",
       "infoBalloonText": "To help us better understand your issue and for a faster resolution please upload the PSR (<a href='https://docs.microsoft.com/office/troubleshoot/settings/how-to-use-problem-steps-recorder'>How to take a PSR</a>)"",
       "required": true,
       "useAsAdditionalDetails": true
      },
      {
       "id": "problem_start_time",
       "order": 3,
       "controlType": "datetimepicker",
       "displayLabel": "Start Date",
       "watermarkText": "When did your issue begin?",
       "required": true
      }
   ]
}
---