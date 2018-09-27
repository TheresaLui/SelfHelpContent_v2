<properties pageTitle="Problem with AAD Domain services enable disable" 
	 description="addomainservicesenabledisable" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32447391" 
	 productPesIds="14785,16576" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with AAD Domain services enable disable 
---
{
  "resourceRequired": false,
  "title": "Problem with AAD Domain services enable disable",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "action",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What action are you trying to perform?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Enable Azure AD Domain Services",
          "value": "enable"
        },
        {
          "text": "Disable Azure AD Domain Services",
          "value": "disable"
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
      "id": "whereEnable",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Where are you trying to perform the task?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Classic Azure Portal",
          "value": "enable"
        },
        {
          "text": "New Azure Portal",
          "value": "disable"
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
      "id": "whichUser",
      "visibility": null,
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Which user is experiencing this problem?",
      "content": null,
      "watermarkText": "Enter user name or Object ID of the user in Azure Active Directory",
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
      "id": "resource",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What Resource ID is experiencing this problem?",
      "content": null,
      "watermarkText": "Note: Resource ID information can be found in the properties blade of your domain service",
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
      "id": "symptoms",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Examples: error message while enabling/disabling Azure AD Domain Services managed domain",
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
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "adDomainServicesEnableDisableadditionalDetails",
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
---