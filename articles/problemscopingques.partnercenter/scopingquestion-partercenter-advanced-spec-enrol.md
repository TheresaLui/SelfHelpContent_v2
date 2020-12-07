<properties
       pageTitle="Advanced Specialization enrollment issues"
       description="Advanced Specialization enrollment issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32725785"
       productPesIds="17000"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_advanced_spec_enrol" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Advanced Specialization enrollment issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Advanced Specialization enrollment issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "advanced_spec",
       "order": 1,
       "visibility": "true",
	   "controlType": "dropdown",
	   "displayLabel": "What is the Advanced Specialization you need help with?",
       "watermarkText":"Please select the Advanced Specialization from the below list",
	   "dropdownOptions": [
	       {
		   "value": "adoption_change",
		   "text": "Adoption and Change Management"
	       },
	       {
		   "value": "calling_msteams",
		   "text": "Calling for Microsoft Teams"
	       },
	       {
		   "value": "datawarehouse_migration_azure",
		   "text": "Data Warehouse Migration to Microsoft Azure"
	       },
	       {
		   "value": "identity_access",
		   "text": "Identity and Access Management"
	       },
	       {
		   "value": "kubernetes_azure",
		   "text": "Kubernetes on Microsoft Azure"
	       },
	       {
		   "value": "linux_azure",
		   "text": "Linux and Open Source Database Migration to Microsoft Azure"
	       },
	       {
		   "value": "meetings_msteams",
		   "text": "Meetings and Meeting Rooms for Microsoft Teams"
	       },
	       {
		   "value": "mswindows_virtual",
		   "text": "Microsoft Windows Virtual Desktop"
	       },
	       {
		   "value": "modernization_webapp_azure",
		   "text": "Modernization of Web Applications to Microsoft Azure"
	       },
	       {
		   "value": "sap_azure",
		   "text": "SAP on Microsoft Azure"
	       },
	       {
		   "value": "teamwork_deploy",
		   "text": "Teamwork Deployment"
	       },
	       {
		   "value": "threat_protection",
		   "text": "Threat Protection"
	       },
	       {
		   "value": "windowsserver_sql_azure",
		   "text": "Windows Server and SQL Server Migration to Microsoft Azure"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
         "id": "text_attach1",
         "visibility": "advanced_spec == sap_azure || advanced_spec == windowsserver_sql_azure",
         "order": 2,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of association, Proof of payment (i.e. Microsoft Invoice), PSR (<a href='https://support.microsoft.com/help/3035258/how-to-use-the-problem-steps-recorder-in-office-365'>How to take a PSR</a>) or Screenshot with the discrepancy, PC Insights Azure usage report."
       },
       {
         "id": "cust_tenant_id1",
         "visibility": "advanced_spec == sap_azure || advanced_spec == windowsserver_sql_azure",
         "controlType": "multilinetextbox",
         "order": 3,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid1",
         "visibility": "advanced_spec == sap_azure || advanced_spec == windowsserver_sql_azure",
         "controlType": "multilinetextbox",
         "order": 4,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name1",
         "visibility": "advanced_spec == sap_azure || advanced_spec == windowsserver_sql_azure",
         "controlType": "multilinetextbox",
         "order": 5,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach2",
         "visibility": "advanced_spec == linux_azure || advanced_spec == datawarehouse_migration_azure",
         "order": 6,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of association, Proof of payment (i.e. Microsoft Invoice), PSR (<a href='https://support.microsoft.com/help/3035258/how-to-use-the-problem-steps-recorder-in-office-365'>How to take a PSR</a>) or Screenshot with the discrepancy, PC Insights Azure usage report."
       },
       {
         "id": "cust_tenant_id2",
         "visibility": "advanced_spec == linux_azure || advanced_spec == datawarehouse_migration_azure",
         "controlType": "multilinetextbox",
         "order": 7,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid2",
         "visibility": "advanced_spec == linux_azure || advanced_spec == datawarehouse_migration_azure",
         "controlType": "multilinetextbox",
         "order": 8,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name2",
         "visibility": "advanced_spec == linux_azure || advanced_spec == datawarehouse_migration_azure",
         "controlType": "multilinetextbox",
         "order": 9,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach3",
         "visibility": "advanced_spec == kubernetes_azure || advanced_spec == modernization_webapp_azure",
         "order": 10,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of association, Proof of payment (i.e. Microsoft Invoice), PSR (<a href='https://support.microsoft.com/help/3035258/how-to-use-the-problem-steps-recorder-in-office-365'>How to take a PSR</a>) or Screenshot with the discrepancy, PC Insights Azure usage report."
       },
       {
         "id": "cust_tenant_id3",
         "visibility": "advanced_spec == kubernetes_azure || advanced_spec == modernization_webapp_azure",
         "controlType": "multilinetextbox",
         "order": 11,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid3",
         "visibility": "advanced_spec == kubernetes_azure || advanced_spec == modernization_webapp_azure",
         "controlType": "multilinetextbox",
         "order": 12,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name3",
         "visibility": "advanced_spec == kubernetes_azure || advanced_spec == modernization_webapp_azure",
         "controlType": "multilinetextbox",
         "order": 13,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach4",
         "visibility": "advanced_spec == mswindows_virtual",
         "order": 14,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of association, Proof of payment (i.e. Microsoft Invoice), PSR (<a href='https://support.microsoft.com/help/3035258/how-to-use-the-problem-steps-recorder-in-office-365'>How to take a PSR</a>) or Screenshot with the discrepancy, PC Insights Azure usage report."
       },
       {
         "id": "cust_tenant_id4",
         "visibility": "advanced_spec == mswindows_virtual",
         "controlType": "multilinetextbox",
         "order": 15,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid4",
         "visibility": "advanced_spec == mswindows_virtual",
         "controlType": "multilinetextbox",
         "order": 16,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name4",
         "visibility": "advanced_spec == mswindows_virtual",
         "controlType": "multilinetextbox",
         "order": 17,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach5",
         "visibility": "advanced_spec == adoption_change || advanced_spec == teamwork_deploy",
         "order": 18,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of payment (Microsoft Invoice), proofs of active usage and proofs submitted during enrollment and date of submission for customer validation"
       },
       {
         "id": "cust_tenant_id5",
         "visibility": "advanced_spec == adoption_change || advanced_spec == teamwork_deploy",
         "controlType": "multilinetextbox",
         "order": 19,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid5",
         "visibility": "advanced_spec == adoption_change || advanced_spec == teamwork_deploy",
         "controlType": "multilinetextbox",
         "order": 20,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name5",
         "visibility": "advanced_spec == adoption_change || advanced_spec == teamwork_deploy",
         "controlType": "multilinetextbox",
         "order": 21,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach6",
         "visibility": "advanced_spec == calling_msteams || advanced_spec == meetings_msteams",
         "order": 22,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of payment (Microsoft Invoice), proofs of active usage and proofs submitted during enrollment and date of submission for customer validation"
       },
       {
         "id": "cust_tenant_id6",
         "visibility": "advanced_spec == calling_msteams || advanced_spec == meetings_msteams",
         "controlType": "multilinetextbox",
         "order": 23,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid6",
         "visibility": "advanced_spec == calling_msteams || advanced_spec == meetings_msteams",
         "controlType": "multilinetextbox",
         "order": 24,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name6",
         "visibility": "advanced_spec == calling_msteams || advanced_spec == meetings_msteams",
         "controlType": "multilinetextbox",
         "order": 25,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "text_attach7",
         "visibility": "advanced_spec == threat_protection || advanced_spec == identity_access",
         "order": 26,
         "controlType": "infoblock",
         "content": "To help us better understand your issue and for a faster resolution please upload the Proof of association, Proof of payment (i.e. Microsoft Invoice) and also proof of active usage"
       },
       {
         "id": "cust_tenant_id7",
         "visibility": "advanced_spec == threat_protection || advanced_spec == identity_access",
         "controlType": "multilinetextbox",
         "order": 27,
         "displayLabel": "Customer Tenant ID",
         "watermarkText": "Please provide the Customer Tenant ID",
         "infoBalloonText": "In case there are multiple Customer Tenant IDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "subscription_guid7",
         "visibility": "advanced_spec == threat_protection || advanced_spec == identity_access",
         "controlType": "multilinetextbox",
         "order": 28,
	     "displayLabel": "Subscription GUID",
	     "watermarkText": "Please provide the Subscription GUID",
         "infoBalloonText": "In case there are multiple Subscription GUIDs that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
         "id": "cust_name7",
         "visibility": "advanced_spec == threat_protection || advanced_spec == identity_access",
         "controlType": "multilinetextbox",
         "order": 29,
	     "displayLabel": "Customer Name",
	     "watermarkText": "Please provide the Customer Name",
         "infoBalloonText": "In case there are multiple Customer Names that do not show revenue acquirement, for a better analysis, please upload an excel file containing all values.",
         "required": false
       },
       {
	   "id": "problem_description",
	   "order": 30,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 31,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
