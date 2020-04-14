<properties
                pageTitle="Application and Service Availability"
                description="Application and Service Availability"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32422589"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0116"
	ownershipId="Compute_CloudServices_Content"
/>
# Availability
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "IIS and ASP.NET errors",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "if_locally",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Does your operation work locally in Compute Emulator?",
            "watermarkText": "Choose an option",
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
                    "value": "I did not try it locally",
                    "text": "I did not try it locally"
                }
            ],
            "required": false
        },
        {
            "id": "if_workaround",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have any workaround which resolves the issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "IIS Reset (for Web role)",
                    "text": "IIS Reset (for Web role)"
                },
                {
                    "value": "Recycling AppPool (for Web role)",
                    "text": "Recycling AppPool (for Web role)"
                },
                {
                    "value": "Rebooting VM (for Web/Worker role)",
                    "text": "Rebooting VM (for Web/Worker role)"
                },
                {
                    "value": "No known workaround",
                    "text": "No known workaround"
                }
            ],
            "required": false
        },
        {
            "id": "error_application",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please specify any errors in the Application, System or Windows Azure event logs.",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "if_codechange",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Did you make any code change recently?",
            "watermarkText": "Choose an option",
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
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
