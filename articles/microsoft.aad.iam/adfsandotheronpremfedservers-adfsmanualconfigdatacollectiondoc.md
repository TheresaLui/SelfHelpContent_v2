<properties pageTitle="Problem with ADFS manual configeration" 
	 description="adfsmanualconfigdatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570968" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with ADFS manual configeration 
---
{
  "resourceRequired": true,
  "title": "Problem with ADFS manual configeration",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "alreadydeployed",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Have you already deployed AD FS?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "ADFSDeployed"
        },
        {
          "text": "No",
          "value": "ADFSNotDeployed"
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
      "id": "versionOfADFS",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What is the version of AD FS farm?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Server 2016",
          "value": "version2016"
        },
        {
          "text": "Server 2012 R2",
          "value": "version2012R2"
        },
        {
          "text": "Server 2012",
          "value": "version2012"
        },
        {
          "text": "Server 2008 R2",
          "value": "version2008R2"
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
      "id": "isMultipleDomain",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Do you want to federate multiple domains with the AD FS farm?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "MultiDomainFederation"
        },
        {
          "text": "No",
          "value": "SingleDomainFederation"
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
      "id": "domainsToFederate",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Which domains need to be federated?",
      "content": null,
      "watermarkText": "Example: Contoso.com,fabrikam.com",
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
      "id": "adfsmanualconfigdatacollectiondocadditionalDetails",
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