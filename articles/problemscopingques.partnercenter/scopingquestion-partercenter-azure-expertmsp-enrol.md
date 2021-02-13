<properties
       pageTitle="Azure Expert MSP enrollment issues"
       description="Azure Expert MSP enrollment issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725787"
       productPesIds="17000"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_azure_expertmsp_enrol" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Azure Expert MSP enrollment issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Azure Expert MSP enrollment issues",
   "fileAttachmentHint": "Please upload a copy if your support contract (if available) also upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "program_enrol",
       "order": 1,
	   "controlType": "dropdown",
	   "displayLabel": "What is the program your company is enrolled in?",
       "watermarkText":"Please select a program from the below list",
	   "dropdownOptions": [
	       {
		   "value": "direct_csp",
		   "text": "Direct CSP"
	       },
	       {
		   "value": "indirect_csp",
		   "text": "Indirect CSP"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
         "id": "csp_tenant",
         "controlType": "multilinetextbox",
         "order": 2,
	     "displayLabel": "CSP Tenant GUID",
	     "watermarkText": "Please provide the CSP Tenant GUID",
         "infoBalloonText": "In case there are multiple CSP Tenant GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_tenant_id",
         "controlType": "multilinetextbox",
         "order": 3,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid",
         "controlType": "multilinetextbox",
         "order": 4,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach",
         "order": 5,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of association, Proof of payment (i.e. Microsoft Invoice), PSR (<a href='https://support.microsoft.com/help/3035258/how-to-use-the-problem-steps-recorder-in-office-365'>How to take a PSR</a>) or Screenshot with the discrepancy, PC Insights Azure usage report."
       },
       {
	   "id": "contract_type",
       "order": 6,
	   "controlType": "dropdown",
	   "displayLabel": "Please select the type of contract you have",
       "watermarkText":"Please select the type of contract from the below list",
	   "dropdownOptions": [
	       {
		   "value": "asfp_contract",
		   "text": "ASFP Contract"
	       },
	       {
		   "value": "psfp_contract",
		   "text": "PSFP Contract"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
         "id": "contract_no",
         "controlType": "textbox",
         "order": 7,
	     "displayLabel": "ASFP or PSFP Contract number",
	     "watermarkText": "Please provide the ASFP or PSFP Contract number",
         "required": false
       },
       {
         "id": "crm_account_id",
         "controlType": "textbox",
         "order": 8,
         "displayLabel": "CRM Account ID",
         "watermarkText": "Please provide the CRM Account ID (if available)",
         "required": false
       },
	   {
	     "id": "organization_id1",
         "order": 9,
	     "controlType": "textbox",
	     "displayLabel": "URL of the published Azure services consulting offer",
	     "watermarkText": "Please provide the URL of the published Azure services consulting offer",
         "infoBalloonText": "Your company should have at least one Azure focused consulting service offer published on one of the following platforms: App Source & Azure Marketplace",
	     "required": false
	   },
       {
	   "id": "problem_description",
	   "order": 10,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 11,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
