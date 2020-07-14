<properties
         pageTitle="Scoping questions for discovery issues"
         description="Scoping questions for discovery issues"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675749"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="18d94ef5-c8b1-448d-bec0-4a05b0bb88eb"
	ownershipId="Compute_AzureMigrate"
/>

# Discovery issues

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Discovery issues",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "access_privileges",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have contributor or access to create Azure resources in subscription?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
{
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "appliance_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the appliance",
            "watermarkText": "E.g. MyContosoAppliance",
            "required": false
        },
         {
            "id": "host_details",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the vCenterServer/Hyper-V host details",
            "watermarkText": "E.g. IP = 172.22.60.1",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
