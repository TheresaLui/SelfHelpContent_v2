<properties pageTitle="Problem assigning licenses to a user" 
description="Problem assigning licenses to a user" 
authors="anmalath" 
selfHelpType="problemassigninglicensetoauser" 
supportTopicIds="32570959" 
productPesIds="14785" 
cloudEnvironments="public" 
schemaVersion="1"/>

{
  "resourceRequired": true,
  "title": "Problem assigning licenses to a user",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whereProblem",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What environment are you using to assign a license to a user?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "gblUse",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Are you using group-based licensing in your tenant to automate license assignment to users?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "gblAndDirectAssignment",
      "visibility": "gblUse!=no",
      "order": 3,
      "controlType": "infoblock",
      "displayLabel": "When users inherit licenses from groups it may not be possible to modify or remove the license from a user. Azure portal displays useful error details in such cases - make sure to click the error notification when your operation fails to find out more. Click here to read about group-based licensing.",
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
      "id": "userId",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the Object ID or user name of the user you are having problems with?",
      "content": null,
      "watermarkText": "The Object ID and user name (user@domain.com) can be found by opening the user in the portal, in the Overview tab in the Essentials box on the very top.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "symptoms",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Additional details that might help us diagnose and solve the problem, such as the name of the product license you are assigning. Consider clicking on the error notification in the portal to display full information about the problem and copy the error details.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "whenBegan",
      "visibility": null,
      "order": 6,
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
      "id": "problemAssigningLicenseToAUseradditionalDetails",
      "visibility": null,
      "order": 7,
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