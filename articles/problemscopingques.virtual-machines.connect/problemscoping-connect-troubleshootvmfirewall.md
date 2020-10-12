<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615534"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0028"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Connect to a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Troubleshoot my VM firewall",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_source",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "From where are you trying to connect?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "On premise",
                    "text": "On premise"
                },
                {
                    "value": "Another machine in Azure",
                    "text": "Another machine in Azure"
                },
                {
                    "value": "Another cloud provider",
                    "text": "Another cloud provider"
                },
                {
                        "value": "Azure Marketplace",
                        "text": "Azure Marketplace"
                }
            ],
            "required": false
        },
        {
            "id": "connect_sourcesubnetip",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your source subnet or IP that you are trying to connect from?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "connect_firewall",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What firewall are you trying to troubleshoot?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows Defender",
                    "text": "Windows Defender"
                },
                {
                    "value": "Third-party firewall",
                    "text": "Third-party firewall"
                }
            ],
            "required": false
        },
        {
            "id": "connect_ifinternet",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do you have connectivity issues from/to this VM?",
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
            "id": "connect_internetissue",
            "order": 5,
            "visibility": "connect_ifinternet == Yes",
            "controlType": "dropdown",
            "displayLabel": "What is the problem you are having?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Cannot connect to the RDP port",
                    "text": "Cannot connect to the RDP port"
                },
                {
                    "value": "Cannot connect to the Powershell port",
                    "text": "Cannot connect to the Powershell port"
                },
                {
                    "value": "Cannot connect to my SQL instance",
                    "text": "Cannot connect to my SQL instance"
                },
                {
                    "value": "Cannot connect to another port",
                    "text": "Cannot connect to another port"
                },
                {
                    "value": "My VM doesn't have access to Internet",
                    "text": "My VM doesn't have access to Internet"
                }
            ],
            "required": false
        },
        {
            "id": "isadmin",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is this the built-in administrator account?",
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
            "id": "name_useraccount",
            "order": 7,
            "visibility": "isadmin == No || isadmin == I do not know",
            "controlType": "textbox",
            "displayLabel": "What is the name of the user account trying to login?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
