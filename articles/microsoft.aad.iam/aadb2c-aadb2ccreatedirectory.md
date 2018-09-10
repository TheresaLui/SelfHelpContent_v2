<properties pageTitle="Problem with AAD B2C create directory" 
	 description="aadb2ccreatedirectory" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32444951" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with AAD B2C create directory 
---
{
  "resourceRequired": false,
  "title": "Problem with AAD B2C create directory",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichTenant",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Which Azure AD B2C tenant are you creating?",
      "content": null,
      "watermarkText": "Enter the name of the tenant (for example: contosoB2C.onmicrosoft.com)",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "whichTool",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Which portal are you using to create this directory?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure portal (portal.azure.com)",
          "value": "azurePortal"
        },
        {
          "text": "Azure classic portal (manage.windowsazure.com)",
          "value": "classicPortal"
        },
        {
          "text": "PowerShell",
          "value": "cantAssign"
        },
        {
          "text": "Other, don't know, or not applicable",
          "value": "other"
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
      "id": "symptoms",
      "visibility": null,
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Examples: error message in the Azure portal",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "whenBegan",
      "visibility": null,
      "order": 4,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem occur?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "aadB2CCreateDirectoryadditionalDetails",
      "visibility": null,
      "order": 5,
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