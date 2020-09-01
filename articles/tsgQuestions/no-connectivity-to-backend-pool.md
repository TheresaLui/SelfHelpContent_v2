<properties
         pageTitle="TSG Workflow Questions - No connectivity to backend pool"
         description="Troubleshoot backend pool issues"
         authors="seanj-ms"
         ms.author="seanj"
         selfHelpType="TSG_Questions"
         productPesIds="15922"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="B3041256-92F9-4DF4-A3C8-F30B804BB1C3"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# TSG Workflow Questions
---
{
    "formElements": [
        {
            "id": "71363d40-dbd3-4282-926c-f3f90932e4a1",
            "order": 1,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is this issue currently happening or is this an RCA request?",
            "radioButtonOptions": [
                {
                    "value": "Issue is still happening",
                    "text": "Issue is still happening"
                },
                {
                    "value": "RCA request",
                    "text": "RCA request"
                }
            ],
            "required": true
        },
        {
            "id": "af9722d8-9393-45f3-aad3-7739119241a7",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "Select load balancer type",
            "radioButtonOptions": [
                {
                    "value": "Basic internal load balancer",
                    "text": "Basic internal load balancer"
                },
                {
                    "value": "Basic external load balancer",
                    "text": "Basic external load balancer"
                },
                {
                    "value": "Standard internal load balancer or Standard external load balancer",
                    "text": "Standard internal load balancer or Standard external load balancer"
                }
            ],
            "required": true
		},
        {
            "id": "611a8b0c-7c28-4e44-97b5-7c97c483d713",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the traffic between virtual networks in different regions?",
            "radioButtonOptions": [
                {
                    "value": "Traffic is globally peered",
                    "text": "Traffic is globally peered"
                },
                {
                    "value": "Traffic is not globally peered",
                    "text": "Traffic is not globally peered"
                }
            ],
            "required": true
		},
        {
            "id": "cb776490-9407-4709-ab06-e7c15219f3c5",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Were there any DIP availability issue at the time of the incident?",
            "radioButtonOptions": [
                {
                    "value": "All DIP VMs were down or Some DIP VMs were down",
                    "text": "All DIP VMs were down or Some DIP VMs were down"
                },
                {
                    "value": "No DIP VMs were down",
                    "text": "No DIP VMs were down"
                }
            ],
            "required": true
		},
        {
            "id": "a71366cd-9834-4705-b7d5-958ce197a75a",
            "order": 5,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is there an NSG blocking SLB health probe?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "02ff2cbb-646e-4512-ab0d-079c811fe1e3",
            "order": 6,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the backend VM online and container settings correct?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "13e9c67c-59a4-40dc-95c5-c3b9f5921462",
            "order": 7,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the customer listening on the port?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "2c87dbbf-e582-4dad-b22e-c68c31006c75",
            "order": 8,
            "controlType": "radioButtonGroup",
            "displayLabel": "Was there traffic passing through the LB at the time of the incident?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "29d36337-f9d0-4a16-9397-bec0dc74d8ef",
            "order": 9,
            "controlType": "radioButtonGroup",
            "displayLabel": "Does the customer have the 'Enable floating IP' property set to True on the load balancing rule?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "fccd1d04-ae94-46d5-91b1-fdd8a8e9a437",
            "order": 10,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is there an NSG blocking the customer source IP?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "0bb97abf-3a88-4daa-ade0-4e01cc135d06",
            "order": 11,
            "controlType": "radioButtonGroup",
            "displayLabel": "Was the Test Traffic routing result RouteTargetInternet_0?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "6090e74d-5d37-4c06-b3a0-26e636fb6010",
            "order": 12,
            "controlType": "radioButtonGroup",
            "displayLabel": "Was the customer able to connect to the VM directly?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
    ],
    "$schema": "SelfHelpContent"
}
---