<properties pageTitle="Problem with administrator initiated password reset" 
	 description="Problem with administrator initiated password reset" 
	 authors="anupnadigm" 
	 selfHelpType="administratorinitiatedpasswordreset" 
	 supportTopicIds="32045781" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with administrator initiated password reset 
---
{
  "resourceRequired": true,
  "title": "Problem with administrator initiated password reset",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "error",
      "visibility": "true",
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "What is the exact error message you see?",
      "content": null,
      "watermarkText": "Please enter what error you see verbatim",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "whichUser",
      "visibility": "true",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Whose password are you having difficulty resetting?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "notAuthorizedForSingleAdmin",
      "visibility": "whichUser==user",
      "order": 3,
      "controlType": "infoblock",
      "displayLabel": "Only administrators can reset user passwords",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "notAuthorizedForMultipleAdmins",
      "visibility": "whichUser==admin",
      "order": 4,
      "controlType": "infoblock",
      "displayLabel": "Only higher privileged administrators can reset other administrator passwords",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "upn",
      "visibility": "true",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Please list all of the affected UPN (User Principal Name)",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 5
    },
    {
      "id": "hasSupportCode",
      "visibility": "true",
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "Do you have a support code/correlation ID for an error related to this problem?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "ifCorrelationID",
      "visibility": "hasSupportCode==yes",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "Support Code/Correlation ID",
      "content": null,
      "watermarkText": "Enter the support code found at the bottom-right of the password reset page",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "getCorrelationID",
      "visibility": "hasSupportCode!=yes",
      "order": 8,
      "controlType": "infoblock",
      "displayLabel": "Microsoft can provide a solution to your problem faster if you can provide the support code found at the bottom-right of the password reset page",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "timeStamp",
      "visibility": "true",
      "order": 9,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "administratorInitiatedPasswordResetadditionalDetails",
      "visibility": null,
      "order": 10,
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