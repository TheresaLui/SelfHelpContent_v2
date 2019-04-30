<properties
                pageTitle="VM Performance"
                description="VM Performance"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615275"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0131"
/>
# VM Performance
---
{
                "subscriptionRequired": true,
                "resourceRequired": true,
                "title": "Replication of Shared Image Version is slow",
                "fileAttachmentHint": "",
                "formElements": [
                {
                  "id": "number_region",
                  "order": 1,
                  "controlType": "textbox",
                  "displayLabel": "How many regions are you replicating your image to?",
                  "required": true
                  },{
                      "id": "image_size",
                      "order": 2,
                      "controlType": "dropdown",
                      "displayLabel": "What is the size of the image?",
                      "watermarkText": "Choose an option",
                      "dropdownOptions": [
                          {
                              "value": "<127GB",
                              "text": "<127GB"
                          },
                          {
                              "value": "127 to 500GB",
                              "text": "127 to 500GB"
                          },
                          {
                              "value": "500GB to 1TB",
                              "text": "500GB to 1TB"
                          },
                          {
                              "value": ">1TB",
                              "text": ">1TB"
                          }
                      ],
                      "required": false
                  },{
                  "id": "problem_description",
                  "order": 3,
                  "controlType": "multilinetextbox",
                  "displayLabel": "Description",
                  "useAsAdditionalDetails": false,
                  "required": true
                  },{
                  "id": "problem_start_time",
                  "order": 4,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem start?",
                  "required": true
                }
                ]
}
---
