<properties 
    pageTitle="Active Directory application access issue"
    description="appsaccessdatacollectiondoc"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32570263"
    productPesIds="16575"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="5c787abf-d198-4bc4-a2f9-4c940c70d8b1"
    />

# Active Directory application access issue

---
{
    "resourceRequired": false,
    "title": "Active Directory application access issue",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whichUser",
            "visibility": null,
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which user or admin is experiencing this problem?",
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
            "id": "problem",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the user or admin trying to accomplish?",
            "content": null,
            "watermarkText": "Examples: trying to create a new application, trying to change application properties, trying to sign in to an application.",
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
            "id": "whereProblem",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Where is the user or admin trying to accomplish this task?",
            "content": null,
            "watermarkText": "Examples: in the Azure portal, on the 'All applications' page in Enterprise Applications; PowerShell; signing in to a custom-developed application",
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
            "id": "symptoms",
            "visibility": null,
            "order": 4,
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
            "id": "whichApp",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Which application is the problem related to?",
            "content": null,
            "watermarkText": "If the problem is with a specific application, enter its display name or object ID here. Or enter 'All apps' or 'Not applicable', if appropriate.",
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
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---