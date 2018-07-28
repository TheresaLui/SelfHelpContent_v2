<properties pageTitle="Problem updating a user" 
	 description="problemupdatinguser" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32565604" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem updating a user 
---
{
  "resourceRequired": true,
  "title": "Problem updating a user",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whatProblem",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Is the problem with updating a single user, or multiple users?",
      "content": null,
      "watermarkText": null,
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
      "id": "targetName",
      "visibility": "whatProblem==single",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "User name",
      "content": null,
      "watermarkText": "Enter the user name ('alice@contoso.com') of the user that cannot be updated.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 1
    },
    {
      "id": "exampleTargetName",
      "visibility": "whatProblem==multiple",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Example user",
      "content": null,
      "watermarkText": "Enter a user name ('alice@contoso.com') for one of the users that cannot be updated..",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 1
    },
    {
      "id": "whereProblem",
      "visibility": null,
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Where does the problem occur?",
      "content": null,
      "watermarkText": null,
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
      "id": "whatSymptom",
      "visibility": null,
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "What is the problem?",
      "content": null,
      "watermarkText": null,
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
      "id": "otherSymptoms",
      "visibility": "whatSymptom==other",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Provide any pertinent details about the problem",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "errorDetails",
      "visibility": "whatSymptom==error",
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Error details",
      "content": null,
      "watermarkText": "Provide any data you can about the error, such as the text of the error message, or a correlation ID",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "whichUser",
      "visibility": null,
      "order": 8,
      "controlType": "textbox",
      "displayLabel": "Who is trying to update this user?",
      "content": null,
      "watermarkText": "Enter user name (such as chris@contoso.com) user in Azure Active Directory",
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
      "id": "whenBegan",
      "visibility": null,
      "order": 9,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem occur (or begin)?",
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
      "id": "problemUpdatingUseradditionalDetails",
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