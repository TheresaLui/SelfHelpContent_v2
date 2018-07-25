<properties pageTitle="Problem with Domains Name verify domain name" 
description="Problem with Domains Name verify domain name" 
authors="anmalath" 
selfHelpType="domainsverifydomainname" 
supportTopicIds="32045779" 
productPesIds="14785" 
cloudEnvironments="public" 
schemaVersion="1"/>

{
  "resourceRequired": true,
  "title": "Problem with Domains Name verify domain name",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichDomain",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "What is the name of the domain that you want to verify?",
      "content": null,
      "watermarkText": "Example 'contoso.com.'",
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
      "id": "whichTenant",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the tenant ID or initial default domain name of the directory in which you want to verify the domain name?",
      "content": null,
      "watermarkText": "The initial default domain name follows the pattern 'contoso.onmicrosoft.com'.",
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
      "id": "symptomType",
      "visibility": null,
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the error that you are receiving?",
      "content": null,
      "watermarkText": null,
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
      "id": "MultiTenant",
      "visibility": null,
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Does your organization use Office 365 with another Azure AD tenant (or otherwise have another Azure AD tenant)?",
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
      "id": "domainsVerifyDomainNameadditionalDetails",
      "visibility": null,
      "order": 5,
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