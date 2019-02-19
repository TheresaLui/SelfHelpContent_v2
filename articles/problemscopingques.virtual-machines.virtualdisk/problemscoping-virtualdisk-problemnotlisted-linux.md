<properties
                pageTitle="Virtual Disk Management"
                description="Virtual Disk Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32632141"
                productPesIds="14749"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0076"
/>
# Virtual Disk Management
---
{
                "resourceRequired": true,
                "title": "My problem is not listed above",
                "fileAttachmentHint": "",
                "formElements": [
                {
                    "id": "virtualdisk_scenario",
                    "order": 1,
                    "controlType": "dropdown",
                    "displayLabel": "Which of the following describes your scenario?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "I want help with my guest os volume",
                            "text": "I want help with my guest os volume"
                        },
                        {
                            "value": "My data inside the temporary drive is lost",
                            "text": "My data inside the temporary drive is lost"
                        },
                        {
                            "value": "I want to find availability set ID or use availability set ID to get storage accounts",
                            "text": "I want to find availability set ID or use availability set ID to get storage accounts"
                        },
                        {
                            "value": "I want to find data about the managed disk",
                            "text": "I want to find data about the managed disk"
                        },
                        {
                            "value": "I want to find provisioning status",
                            "text": "I want to find provisioning status"
                        },
                        {
                            "value": "Other (describe below)",
                            "text": "Other (describe below)"
                        }
                    ],
                    "required": false
                },{
                    "id": "virtualdisk_operation",
                    "order": 2,
                    "visibility": "virtualdisk_scenario == I want help with my guest os volume",
                    "controlType": "dropdown",
                    "displayLabel": "What is the operation you are trying to perform?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Create or expand a storage pool configuration",
                            "text": "Create or expand a storage pool configuration"
                        },
                        {
                            "value": "Expand Windows volume",
                            "text": "Expand Windows volume"
                        },
                        {
                            "value": "Other (describe below)",
                            "text": "Other (describe below)"
                        }
                    ],
                    "required": false
                },{
                    "id": "virtualdisk_availabilityid_operation",
                    "order": 3,
                    "visibility": "virtualdisk_scenario == I want to find availability set ID or use availability set ID to get storage accounts",
                    "controlType": "dropdown",
                    "displayLabel": "What is the operation you are trying to perform?",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Find availability set ID",
                            "text": "Find availability set ID"
                        },
                        {
                            "value": "Use availability set ID to get storage accounts",
                            "text": "Use availability set ID to get storage accounts"
                        },
                        {
                            "value": "Other (describe below)",
                            "text": "Other (describe below)"
                        }
                    ],
                    "required": false
                },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": true,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 5,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
