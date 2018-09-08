<properties pageTitle="Problem creating a user or group" 
	 description="problemcreatinguserorgroup" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32586792" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem creating a user or group 
---
{
  "resourceRequired": false,
  "title": "Problem creating a user or group",
  "fileAttachmentHint": "Screenshot of problem",
  "formElements": [
    {
      "id": "resourceType",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Is the problem creating a user or a group?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "User",
          "value": "user"
        },
        {
          "text": "Group",
          "value": "group"
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
      "id": "notB2b",
      "visibility": null,
      "order": 2,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "If the problem has to do with inviting guest users to collaborate with your organization, please go to the previous step and select the category 'Adding a guest user(B2B)'.'",
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
      "id": "whichUser",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Which user is experiencing the problem?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Me",
          "value": "self"
        },
        {
          "text": "Another user",
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
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "What is the user name of the user who is having the problem?",
      "content": null,
      "watermarkText": "Enter user name (such as alice@contoso.com) or Object ID of the user in Azure Active Directory",
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
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "Where does the problem occur?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure portal",
          "value": "azurePortal"
        },
        {
          "text": "PowerShell",
          "value": "powerShell"
        },
        {
          "text": "Access panel",
          "value": "accesPanel"
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
      "id": "symptoms",
      "visibility": null,
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Examples: error message in the Azure portal, add button not enabled",
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
      "order": 7,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
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
      "id": "problemCreatingUserOrGroupadditionalDetails",
      "visibility": null,
      "order": 8,
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