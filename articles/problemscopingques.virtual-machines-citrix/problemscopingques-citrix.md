<properties
         pageTitle="Virtual Machine running Citrix"
         description="Virtual Machine running Citrix"
         authors="summertgu"
         ms.author="tiag"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32567269, 32567274, 32567278, 32567282, 32567271, 32567276, 32567280, 32567285"
         productPesIds="16215"
         cloudEnvironments="Public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="b4b6273d-558e-4f2d-ab00-36a830ea67"
	ownershipId="Compute_VirtualMachines"
/>
# Citrix VM
---
{
                "subscriptionRequired": true,
                "resourceRequired": false,
                "fileAttachmentHint": "",
                "formElements": [
        {
            "id": "citrixcase",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have a support case with Citrix?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "citrixcase_id",
            "order": 2,
            "visibility": "citrixcase == Yes",
            "controlType": "textbox",
            "displayLabel": "Citrix support case number",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
