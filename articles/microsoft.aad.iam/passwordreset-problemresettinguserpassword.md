<properties pageTitle="User-initiated password reset" 
	 description="Password Management/User-initiated password reset" 
	 authors="sahenry" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32615416,32615432" 
	 productPesIds="16579" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
	 articleId="c0816905-886c-41cc-acab-516a43988111"
/> 
# Problem with user-initiated password reset 
---
{
  "resourceRequired": false,
  "title": "Problem with password management user-initiated",
  "fileAttachmentHint": null,
  "formElements": [
	{
      "id": "correlationId",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Correlation ID from Error message:",
      "content": null,
      "watermarkText": "Copy the correlation ID from the error message and paste it here",
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
      "id": "timestamp",
      "visibility": null,
      "order": 2,
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
      "id": "userNameOrId",
      "visibility": null,
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Which user is experiencing this problem?",
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
      "id": "errorMessageAdditionalDetails",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "If you received an error, please provide the error message details:",
      "content": null,
      "watermarkText":  "AADSTSXXXXX: error message, Error message from the application, etc... ",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": true,
      "numberOfLines": 3
    }
  ]
}
---