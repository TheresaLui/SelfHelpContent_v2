<properties
         pageTitle="Virtual Machine running Citrix"
         description="Virtual Machine running Citrix"
         authors="summertgu"
         ms.author="tiag"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32567270, 32567275, 32567279, 32567283"
         productPesIds="16215"
         cloudEnvironments="Public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="b4b6273d-558e-4f2d-ab00-36a830ea68"
	ownershipId="Compute_VirtualMachines"
/>
# Citrix VM Connectivity
---
{
                "subscriptionRequired": true,
                "resourceRequired": false,
                "title": "Connectivity",
                "fileAttachmentHint": "",
                "formElements": [
        {
            "id": "problems_scenario_connect",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please specify your issue.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "My configuration change impacted connectivity",
                    "text": "My configuration change impacted connectivity"
                },
                {
                    "value": "Troubleshoot my network security group (NSG)",
                    "text": "Troubleshoot my network security group (NSG)"
                },
                {
                    "value": "Troubleshoot my VM firewall",
                    "text": "Troubleshoot my VM firewall"
                },
                {
                    "value": "I have an issue with my public IP",
                    "text": "I have an issue with my public IP"
                },
                {
                    "value": "My VM is not booting",
                    "text": "My VM is not booting"
                },
                {
                    "value": "I need to reset my password",
                    "text": "I need to reset my password"
                },
                {
                    "value": "I need guidance with serial console access",
                    "text": "I need guidance with serial console access"
                },
                {
                    "value": "Failure to connect using RDP or SSH port",
                    "text": "Failure to connect using RDP or SSH port"
                },
                {
                    "value": "My problem is not listed above",
                    "text": "My problem is not listed above"
                }
            ],
            "required": false
        },
        {
            "id": "citrixcase",
            "order": 2,
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
            "order": 3,
            "visibility": "citrixcase == Yes",
            "controlType": "textbox",
            "displayLabel": "Citrix support case number",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
