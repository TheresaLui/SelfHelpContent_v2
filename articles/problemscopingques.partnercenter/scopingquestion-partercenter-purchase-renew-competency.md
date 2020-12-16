<properties
       pageTitle="Purchase or renew Silver or Gold Competency issues"
       description="Purchase or renew Silver or Gold Competency intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725876"
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_purchase_renew_competency" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Purchase or renew Silver or Gold Competency issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Purchase or renew Silver or Gold Competency issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
   "formElements": [
       {
         "id": "learn_more",
         "order": 1,
         "controlType": "infoblock",
         "content": "If you have questions or issues related to payment transaction, before ending the process, please complete this ticket submission. If you have already completed the payment and you need help with a refund or there is a delay in activating the membership, depending on your issue, please use one of the MPN - Billing and Invoicing templates. (To access these templates please go on the top of this page, click on the 'Select a different issue', than click 'Browse topics'. Select the MPN value from 'Category' dropdown, than select the Billing and Invoicing value from the 'Topic' dropdown and a 'Subtopic' based on your issue. Once you complete this selection click on the 'Review solutions' button.)"
       },
       {
	     "id": "support_level",
         "order": 2,
	     "controlType": "dropdown",
	     "displayLabel": "What is the level of support you have payment related question for?",
         "watermarkText":"Please select a level of support from the below list",
	     "dropdownOptions": [
	       {
		   "value": "gold_level",
		   "text": "Gold"
	       },
	       {
		   "value": "silver_level",
		   "text": "Silver"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "payment_method",
       "order": 3,
	   "controlType": "dropdown",
	   "displayLabel": "What method of payment is your question related to?",
       "watermarkText":"Please select a method of payment from the below list",
	   "dropdownOptions": [
	       {
		   "value": "credit_card",
		   "text": "Credit Card"
	       },
	       {
		   "value": "electronic_transfer",
		   "text": "Electronic Transfer"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 4,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any additional information about your issue",
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
