<properties 
    pageTitle="Administrator-initiated password reset" 
	description="Password Management/Administrator-initiated password reset" 
	authors="sahenry" 
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32045781" 
	productPesIds="16579" 
	cloudEnvironments="public" 
	schemaVersion="1"
    articleId="5b936215-dc2e-45df-b66d-d2214ae748a5"
/> 
# Problem with administrator-initiated password reset 
---
{
  "resourceRequired": false,
  "title": "Problem with password management administrator-initiated",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "adminUserNameOrId",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "What is the username of the admin who is resetting the user's password?",
      "content": null,
      "watermarkText": "For example 'sarah@contoso.com'",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": true,
      "numberOfLines": 0
    },
	{
      "id": "userNameOrId",
      "visibility": null,
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What is the username of the user whose password the admin is trying to reset?",
      "content": null,
      "watermarkText": "For example 'joe@contoso.com'.",
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
      "id": "timestamp",
      "visibility": null,
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Timestamp from Error message:",
      "content": null,
      "watermarkText": "Copy the timestamp from the error message and paste it here",
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
      "id": "symptomType",
      "visibility": null,
      "order": 4,
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
    }
  ]
}
---