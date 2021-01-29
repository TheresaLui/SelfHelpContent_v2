<properties pageTitle="SQL Database Backup or Restore is Slow"
	 description="SQL Database Backup or Restore is Slow"
         ms.author="ujpat,amamun,vadeveka"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32748893"
	 productPesIds="14745,16342"
	 cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	 schemaVersion="1"
	 articleId="d92d5aaa-98d2-44c7-970c-a9df074c48b4"
	 ownershipId="AzureData_AzureSQLVM"
/>
# SQL Database Backup or Restore is Slow
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": false,
  "subscriptionRequired": false,
  "title": "SQL Database Backup or Restore is Slow.",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start",
      "required": true
    },
    {
      "id": "What_Area",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What operation is slow?",
      "watermarkText": "Choose an option",
      "content": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Backup Database",
          "value": "bckup"
        },
        {
          "text": "Restore Database",
          "value": "restore"
        },
        {
          "text": "I’m not sure/don’t know",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "Area_Compare",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Is the Backup or Restore faster on another machine?",
      "watermarkText": "Choose an option",
      "content": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "yes"
        },
        {
          "text": "No",
          "value": "no"
        },
        {
          "text": "I’m not sure/don’t know",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "problem_description",
      "order": 1000,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true
    }
  ],
  "$schema": "SelfHelpContent"
}
---
