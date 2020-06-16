<properties pageTitle="Problem with AAD Domain services vnet" 
	 description="addomainservicesvnetissues" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570966" 
	 productPesIds="14785,16576" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="55a6eeda-9d80-41bb-aabc-88a98677b559"
	ownershipId="AzureIdentity_AzureActiveDirectoryDomainServices"
/> 
# Problem with AAD Domain services vnet 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD Domain services vnet",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "PREVIEW: Get help from our intelligent knowledge base",
        "description": "Our self-service troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "We did not find a match for your specific problem in our knowledge base. See links below for other info that may address your problem."
    },
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
            "hints": [],
            "required": false,
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
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "userInput",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the user trying to accomplish?",
            "content": null,
            "watermarkText": "Examples: trying to modify the virtual network, trying to update the DNS settings",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Examples: error message while logging into a computer joined to the managed domain",
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
            "id": "problem_start_time",
            "visibility": null,
            "order": 5,
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
            "id": "problem_description",
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
    ],
    "$schema": "SelfHelpContent"
}
---