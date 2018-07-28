<properties pageTitle="Other Problem with AAD B2C" 
	 description="aadb2cotherproblem" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570973" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Other Problem with AAD B2C 
---
{
  "resourceRequired": true,
  "title": "Other Problem with AAD B2C",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichTenant",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Which Azure AD B2C tenant are you using?",
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
      "id": "appRegistrationStyle",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "How did you register the application that you are using?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Via the Azure AD B2C Applications Menu",
          "value": "B2CPortal"
        },
        {
          "text": "Via PowerShell",
          "value": "Powershell"
        },
        {
          "text": "Through identity.microsoft.com",
          "value": "ARP"
        },
        {
          "text": "Don't know",
          "value": "Other"
        }
      ],
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "getAppRegistration",
      "visibility": "appRegistrationStyle!=B2CPortal",
      "order": 3,
      "controlType": "infoblock",
      "displayLabel": "All Azure AD B2C applications need to be registered through the Azure portal.",
      "content": "<a href=''>All Azure AD B2C applications need to be registered through the Azure portal.</a>",
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
      "id": "appId",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the application ID experiencing this problem?",
      "content": null,
      "watermarkText": "Application ID is in the Properties section in the Azure AD B2C configuration for the application",
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
      "id": "correlationId",
      "visibility": null,
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "Correlation ID",
      "content": null,
      "watermarkText": "Enter the correlation ID if one was shown when a user attempted to sign in",
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
      "id": "symptoms",
      "visibility": null,
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Examples: error message in the Azure portal, error message on signing in, incorrect data on application properties page",
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
      "id": "aadB2COtherProblemadditionalDetails",
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