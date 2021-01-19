<properties
 articleId="problemscopingques-sqlmi-distributed-transactions"
 pageTitle="Azure SQL Managed Instance"
 description="Scoping questions to get more details about distributed-transactions issue"
 authors="vtpombei"
 authoralias="vtpombei"
 ms.author="vtpombei"
 selfHelpType="problemScopingQuestions"
 productPesIds="16259"
 supportTopicIds="32749585"
 cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
 schemaVersion="1"
 ownershipId="AzureData_AzureSQLMI" 
/>

# Azure SQL Managed Instance
---
{
 "$schema": "SelfHelpContent",
 "subscriptionRequired": true,
 "resourceRequired": false,
 "title": "Distributed transactions",
 "fileAttachmentHint": "",
 "formElements": [
 {
  "id": "problem_start_time",
  "order": 1,
  "controlType": "datetimepicker",
  "displayLabel": "When did you face the issue?",
  "required": true
 },
 {
  "id": "type_issue",
  "order": 10,
  "controlType": "dropdown",
  "displayLabel": "What type of issue are you facing",
  "watermarkText": "Choose an option",
  "dropdownOptions": [
   { "value": "msdtc-not-available",
     "text": "MSDTC not available error"
   },
   {
    "value": "dt-connectivity",
	"text": "Distributed transactions connectivity issue"
   },
   {
    "value": "dt-security",
	"text": "Distributed transactions security issue"
   },
   {
    "value": "dont_know_answer",
	"text": "Don't know the answer or issue not listed"
   }
  ],
  "required": true
 },
 {
  "id": "first_instance",
  "order": 20,
  "controlType": "dropdown",
  "displayLabel": "First Managed Instance participating in distributed transaction scenario",
  "watermarkText": "Choose an option",
  "dynamicDropdownOptions": {
   "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/managedInstances?api-version=2018-06-01-preview",
   "jTokenPath": "value",
   "textProperty": "name",
   "valueProperty": "id",
   "textPropertyRegex": "[^/]+$",
   "defaultDropdownOptions": {
    "value": "dont_know_answer",
	"text": "Other, don't know or not applicable"
   }
  },
  "dropdownOptions": [
   {
    "value": "no_list",
	"text": "Unable to get the list of instances"
   }
  ],
  "required": true
 },
 {
  "id": "second_instance",
  "order": 30,
  "controlType": "dropdown",
  "displayLabel": "Second Managed Instance participating in distributed transaction scenario",
  "watermarkText": "Choose an option",
  "dynamicDropdownOptions": {
   "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/managedInstances?api-version=2018-06-01-preview",
   "jTokenPath": "value",
   "textProperty": "name",
   "valueProperty": "id",
   "textPropertyRegex": "[^/]+$",
   "defaultDropdownOptions": {
    "value": "dont_know_answer",
	"text": "Other, don't know or not applicable"
   }
  },
  "dropdownOptions": [
   {
    "value": "no_list",
	"text": "Unable to get the list of instances"
   }
  ],
  "required": true
 },
 {
  "id": "problem_description",
  "order": 99,
  "controlType": "multilinetextbox",
  "useAsAdditionalDetails": true,
  "displayLabel": "Details of the issue.",
  "watermarkText": "Please provide additional context for the issue you are encountering",
  "required": true
 }
 ]
}
---
