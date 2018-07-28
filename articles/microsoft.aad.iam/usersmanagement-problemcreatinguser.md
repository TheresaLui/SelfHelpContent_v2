<properties pageTitle="Problem creating a user" 
	 description="problemcreatinguser" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32045780" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem creating a user 
---
{
  "resourceRequired": true,
  "title": "Problem creating a user",
  "fileAttachmentHint": "Screenshot of problem",
  "formElements": [
    {
      "id": "notB2b",
      "visibility": null,
      "order": 1,
      "controlType": "infoblock",
      "displayLabel": "If the problem has to do with inviting guest users to collaborate with your organization, please go to the previous step and select the category 'Adding a guest user(B2B)'.'",
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
      "id": "whereProblem",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Where does the problem occur?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure portal (portal.azure.com)",
          "value": "azurePortal"
        },
        {
          "text": "classic Azure portal (manage.windowsazure.com)",
          "value": "classicPortal"
        },
        {
          "text": "PowerShell",
          "value": "powerShell"
        },
        {
          "text": "Other, don't know or not applicable",
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
      "id": "whatProblem",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "What is the problem?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "I can't find where to add a new user to Azure AD",
          "value": "cantFind"
        },
        {
          "text": "The 'new' button isn't enabled",
          "value": "notEnabled"
        },
        {
          "text": "Error during creation of a user",
          "value": "serverError"
        },
        {
          "text": "Other, don't know or not applicable",
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
      "id": "otherSymptoms",
      "visibility": "whatProblem==other",
      "order": 4,
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
      "visibility": "whatProblem==serverError",
      "order": 5,
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
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "Which administrator is experiencing the problem?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Me",
          "value": "self"
        },
        {
          "text": "Another administrator",
          "value": "otherUser"
        },
        {
          "text": "Other, don't know or not applicable",
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
      "id": "whichOtherUser",
      "visibility": "whichUser==otherUser",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "Which administrator is having a problem creating a user?",
      "content": null,
      "watermarkText": "Enter user name (such as alice@contoso.com) of the administrator",
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
      "order": 8,
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
      "id": "problemCreatingUseradditionalDetails",
      "visibility": null,
      "order": 9,
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