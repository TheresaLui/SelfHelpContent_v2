<properties
	pageTitle="Azure SQL Managed Instance"
	description="Scoping questions to get more details about server trust group issue"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749584"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sqlmi-server-trust-group"
	ownershipId="AzureData_AzureSQLMI"
/>

# Azure SQL Managed Instance
---
{
 "$schema": "SelfHelpContent",
 "subscriptionRequired": true,
 "resourceRequired": false,
 "title": "Server Trust Group",
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
 {
 "value": "server-trust-group-setup-issue",
 "text": "Server trust group setup issue"
 },
 {
 "value": "dont_know_answer",
 "text": "Don't know the answer or issue not listed"
 }
 ],
 "required": true
 },
 {
 "id": "server_trust_group_name",
 "order": 15,
 "controlType": "textbox",
 "displayLabel": "Server trust group name",
 "infoBalloonText": "Please provide the name of the affected Server trust group.",
 "infoBalloonText": "",
 "required": true,
 "content": null,
 "maxLength": 0,
 "useAsAdditionalDetails": false,
 "numberOfLines": 0
 },
 {
 "id": "first_instance",
 "order": 20,
 "controlType": "dropdown",
 "displayLabel": "First member of the trust group",
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
 "displayLabel": "Second member of the trust group",
 "watermarkText": "Choose an option",
 "dynamicDropdownOptions": { "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/managedInstances?api-version=2018-06-01-preview",
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
