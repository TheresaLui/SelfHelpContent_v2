<properties pageTitle="Cannot find a SQL Image"
	 description="Cannot find a SQL Image"
         ms.author="ujpat,amamun,vadeveka"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32773092"
	 productPesIds="14745,16342"
	 cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	 schemaVersion="1"
	 articleId="eb307258-741b-4d24-a264-e2edc50bb313"
	 ownershipId="AzureData_AzureSQLVM"
/>
# Cannot find a SQL Image
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": false,
  "subscriptionRequired": false,
  "title": "Cannot find a SQL Image",
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
      "id": "Which_Version",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What version of SQL Server image are you looking for?",
      "watermarkText": "Choose an option",
      "content": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text":"SQL Server 2008/R2",
          "value":"2008"
        },
        {
          "text":"SQL Server 2012",
          "value":"2012"
        },
        {
          "text":"SQL Server 2014",
          "value":"2014"
        },
        {
	  "text":"SQL Server 2016",
	   "value":"2016"
        },
        {
	   "text": "SQL Server 2017",
	   "value": "2017"
        },
        {
	   "text":"SQL Server 2019",
	   "value":"2019"
        },
        {
          "text":"I’m not sure/don’t know",
          "value":"dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "Which_way",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Please let us know what platform are you using to deploy?",
      "watermarkText": "Choose an option",
      "content": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text":"Azure Portal",
          "value":"AP"
        },
        {
          "text":"PowerShell",
          "value":"PS"
        },
        {
	 "text":"Azure CLI",
	 "value":"CLI"
        },
        {
          "text":"I’m not sure/don’t know",
          "value":"dont_know_answer"
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
