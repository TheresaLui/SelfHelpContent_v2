<properties pageTitle="Problem with Deleting directory other problem" 
	 description="problemdeletingazureadother" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32565596" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with Deleting directory other problem 
---
{
  "resourceRequired": true,
  "title": "Problem with Deleting directory other problem",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichDirectory",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "What is the name of the directory or initial .onmicrosoft.com domain for the Azure AD that fails to delete?",
      "content": null,
      "watermarkText": "For example 'contoso.onmicrosoft.com.'",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "symptomType",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the error that you are receiving?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "MultiTenant",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Does your organization have another Azure AD or use Office 365?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "No additional directories",
          "value": "None"
        },
        {
          "text": "Yes we have an additional Azure AD or use Office 365",
          "value": "ContainsMultiple"
        }
      ],
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "ProblemDeletingAzureADOtheradditionalDetails",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional details",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": true,
      "numberOfLines": 0
    }
  ]
}
---