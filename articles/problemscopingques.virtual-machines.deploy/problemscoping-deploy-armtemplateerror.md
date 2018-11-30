<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="summertgu"
                authorAlias="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628255"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea1212"
/>
# Deploy a VM
---
{
    "resourceRequired": true,
    "title": "Troubleshoot my ARM template error",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "deployment_manageddisks",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying with managed disks?",
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
        },{
            "id": "deployment_method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How are you deploying your template?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "ARM",
                    "text": "ARM"
                },
                {
                    "value": "Powershell",
                    "text": "Powershell"
                },
                {
                    "value": "CLI",
                    "text": "CLI"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },{
            "id": "deployment_fromgithub",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is your template from github?",
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
        },{
                  "id": "github_link",
                  "order": 4,
                  "visibility": "deployment_fromgithub == Yes",
                  "controlType": "multilinetextbox",
                  "displayLabel": "Link to template on github",
                  "useAsAdditionalDetails": true,
                  "required": true
                  },{
                  "id": "correlation_id",
                  "order": 5,
                  "controlType": "textbox",
                  "displayLabel": "Correlation ID",
                  "useAsAdditionalDetails": false,
                  "required": false
                  },{
                  "id": "problem_description",
                  "order": 6,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  }
    ]
}
---
