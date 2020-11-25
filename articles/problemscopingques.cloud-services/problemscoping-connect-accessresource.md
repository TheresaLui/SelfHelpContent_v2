<properties
                pageTitle="Connectivity"
                description="Connectivity"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32565483"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0114"
	ownershipId="Compute_CloudServices_Content"
/>
# Connectivity
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem that is related to accessing resources from Cloud Services",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cloud_service_slots",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Slot",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [{
                "value": "Production",
                "text": "Production"
            }, {
                "value": "Staging",
                "text": "Staging"
            }]
        },
        {
            "id": "cloud_service_roles",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Role",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "cloud_service_slots != null && cloud_service_slots != dont_know_answer",
            "dynamicDropdownOptions": {
                "dependsOn": "cloud_service_slots",
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.classiccompute/domainnames/{resourceName}/slots/{replaceWithParentValue}/roles?&api-version=2015-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No roles available"
                }
            }
        },
        {
            "id": "resource_url",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What resource you are trying to connect to? Can you provide a URL of the resource?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you receive when you try to connect to the resource from Cloud Service?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "network_trace",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Did you collect any network traces during connectivity issue? If yes, please upload them and share the client IP address.",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
