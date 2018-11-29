<properties pageTitle="Problem with AAD Domain services user sign in" 
	 description="addomainservicesusersigninissues" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570965" 
	 productPesIds="14785,16576" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
    articleId="c6907ac8-9424-45b2-9a8e-5432c51fe44c"
/> 
# Problem with AAD Domain services user sign in 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD Domain services user sign in",
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
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "userType",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the affected user synced from on-prem or is it cloud-only user?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Synced",
                    "value": "Synced"
                },
                {
                    "text": "Cloud-only",
                    "value": "CloudOnly"
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
            "id": "resource",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Which Resource ID is experiencing this problem?",
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
            "id": "problem",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the user trying to accomplish?",
            "content": null,
            "watermarkText": "Examples: trying to add a computer/user to the managed domain.",
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
            "watermarkText": "Examples: error message while logging into a computer joined to the managed domain",
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
            "id": "problem_start_time",
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
            "id": "problem_description",
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