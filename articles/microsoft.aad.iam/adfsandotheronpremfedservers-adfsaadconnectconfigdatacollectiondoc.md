<properties pageTitle="Problem with ADFS AD connect configeration" 
	 description="adfsaadconnectconfigdatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570969" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with ADFS AD connect configeration 
---
{
  "resourceRequired": false,
  "title": "Problem with ADFS AD connect configeration",
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
          "value": "ADSFSDeployed"
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
          "value": "singleDomainFederation"
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