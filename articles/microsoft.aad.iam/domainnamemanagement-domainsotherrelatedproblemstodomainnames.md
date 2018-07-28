<properties pageTitle="Other related problem with Domain Names" 
	 description="domainsotherrelatedproblemstodomainnames" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32565597" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Other related problem with Domain Names 
---
{
  "resourceRequired": true,
  "title": "Other related problem with Domain Names",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichDomain",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "What is the custom domain name that you are having issues with?",
      "content": null,
      "watermarkText": "For example 'contoso.com.'",
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
      "id": "whichTenant",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the tenantID or intial default domain name of the directory that fails to add or delete the domain?",
      "content": null,
      "watermarkText": "The initial default domain name is something like 'contoso.onmicrosoft.com'.",
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
      "hints": [],
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
      "displayLabel": "Does your organization have another Azure AD or use Office 365?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "No additional directories",
          "value": "None"
        },
        {
          "text": "Yes we have an additional Azure AD or use Office 365",
          "value": "ContainsMultiple"
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
      "id": "domainsOtherRelatedProblemsToDomainNamesadditionalDetails",
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
---