<properties
    pageTitle="claims"
    description="Problem with the Sample Claims Provider"
    authors="jbeman"
    ms.author="jbeman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32725755"
    productPesIds="16918"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-coreclaims"
	ownershipId="AzureIot_Mobility"
/>

# Problem with the Sample Claims Provider

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with the Sample Claims Provider",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem occur?",
            "required": false
        },
        {
            "id": "problem_region",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which region is your VM and/or cluster located?",
            "watermarkText": "Azure Region",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe your problem",
            "watermarkText": "Problem description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "deployment_type",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "What type of deployment are you working on?",
            "dropdownOptions": [{
                    "value": "DevSetup",
                    "text": "DevSetup (Partner Kit)"
                }, {
                    "value": "EasyButton",
                    "text": "EasyButton"
                }, {
                    "value": "Test_Cluster",
                    "text": "Test Cluster"
                },{
                    "value": "Production",
                    "text": "Production"
                },  {
                    "text": "I don't know",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "version",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What version of MCVP core are you attempting to deploy?",
            "required": true
        },
        {
            "id": "sample_claims_or_service",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Are you having issues with the sample claims provider service, or adding, deleting, or modifying claims to the system?",
            "dropdownOptions": [{
                "value": "Claims_Service",
                "text": "Claims Service"
                }, {
                    "value": "Adding_Claims",
                    "text": "Adding Claims"
                }, {
                    "value": "Deleting_Claims",
                    "text": "Deleting Claims"
                }, {
                    "value": "Modifying_Claims",
                    "text": "Modifying Claims"
                }
                ,{
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "built_claims_service",
            "order": 7,
            "controlType": "radiobuttongroup",
            "displayLabel": "Did you build the sample claims provider before running it?",
           "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
