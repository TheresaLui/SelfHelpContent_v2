<properties pageTitle="Problem with AAD Domain services ldaps" 
description="Problem with AAD Domain services ldaps" 
authors="anmalath" 
selfHelpType="addomainservicesissuesldaps" 
supportTopicIds="32570967" 
productPesIds="14785" 
cloudEnvironments="public" 
schemaVersion="1"/>

{
  "resourceRequired": true,
  "title": "Problem with AAD Domain services ldaps",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichUser",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Which user is experiencing this problem?",
      "content": null,
      "watermarkText": "Enter user name or Object ID of the user in Azure Active Directory",
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
      "id": "resource",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Which Resource ID is experiencing this problem?",
      "content": null,
      "watermarkText": "Note: Resource ID information can be found in the properties blade of your domain service",
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
      "id": "problem",
      "visibility": null,
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the user trying to accomplish?",
      "content": null,
      "watermarkText": "Examples: trying to enable/disable Secure LDAP on Azure AD Domain Services, trying to enable/disable secure LDAP access over the internet.",
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
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Examples: error message while enabling secure LDAP",
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
      "id": "whenBegan",
      "visibility": null,
      "order": 5,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
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
      "id": "adDomainServicesIssuesLDAPSadditionalDetails",
      "visibility": null,
      "order": 6,
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