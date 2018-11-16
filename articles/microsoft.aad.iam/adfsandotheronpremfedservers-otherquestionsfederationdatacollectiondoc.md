<properties pageTitle="Other problems with ADFS" 
	 description="otherquestionsfederationdatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32565603" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Other problems with ADFS 
---
{
  "resourceRequired": false,
  "title": "Other problems with ADFS",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "userUPN",
      "visibility": null,
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "UPN of one of the affected users?",
      "content": null,
      "watermarkText": "Example: user@contoso.com",
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
      "id": "federatedDomain",
      "visibility": null,
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "If there is a particular domain having issues with federation, provide the domain name.",
      "content": null,
      "watermarkText": "Example: contoso.com",
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
      "id": "federationProduct",
      "visibility": null,
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the federation product used?",
      "content": null,
      "watermarkText": "Example: Ping / Siteminder etc.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 1
    },
    {
      "id": "problem_description",
      "visibility": null,
      "order": 4,
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