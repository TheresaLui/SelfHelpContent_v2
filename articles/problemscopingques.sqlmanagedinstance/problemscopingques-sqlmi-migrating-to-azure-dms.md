<properties
	articleId="problemscopingques-sqlmi-migrating-to-azure-dms"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture dms issues"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637255"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
   "$schema":"SelfHelpContent",
   "resourceRequired":false,
   "subscriptionRequired":false,
   "title":"Database Migration Service (DMS)",
   "fileAttachmentHint":"",
   "formElements":[
      {
         "id":"problem_start_time",
         "order":1,
         "controlType":"datetimepicker",
         "displayLabel":"When did the problem start?",
         "required":true
      },
      {
         "id":"issue_type",
         "order":10,
         "controlType":"dropdown",
         "displayLabel":"What kind of issue are you facing?",
         "watermarkText":"Choose an option",
         "infoBalloonText":"Choose the type of issue",
         "dropdownOptions":[
            {
               "value":"advisory",
               "text":"Advisory or questions"
            },
            {
               "value":"provision",
               "text":"Provisioning the DMS resource"
            },
            {
               "value":"managing",
               "text":"Managing DMS projects (create, update or delete)"
            },
            {
               "value":"migrating",
               "text":"Running a DMS project"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer, another kind of issue"
            }
         ],
         "required":true
      },
      {
         "id":"dms_region",
         "order":20,
         "controlType":"textbox",
         "visibility":"issue_type == provision",
         "displayLabel":"In what Azure region are you trying to provision DMS?",
         "required":false
      },
      {
         "id":"service_mode",
         "order":21,
         "controlType":"dropdown",
         "visibility":"issue_type == provision",
         "displayLabel":"What is the service mode being selected?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"azure",
               "text":"Azure"
            },
            {
               "value":"hybrid",
               "text":"Hybrid"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer, any of them"
            }
         ],
         "required":true
      },
      {
         "id":"dms_vnet",
         "order":22,
         "controlType":"textbox",
         "visibility":"issue_type == provision",
         "displayLabel":"What is the VNet and Subnet being used?",
         "required":false
      },
      {
         "id":"migrating_issue_type",
         "order":30,
         "controlType":"dropdown",
         "visibility":"issue_type == migrating",
         "displayLabel":"What kind of issue are you facing when running the project?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"connect_source",
               "text":"Can't connect to source"
            },
            {
               "value":"long_running",
               "text":"Slow migration"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer, other kinf of issue"
            }
         ],
         "required":false
      },
      {
         "id":"source_engine",
         "order":32,
         "controlType":"dropdown",
         "visibility":"issue_type == migrating || issue_type == managing",
         "displayLabel":"What the database engine on the source?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"sql",
               "text":"Sql Server"
            },
            {
               "value":"aws_sql",
               "text":"AWS RDS for SQL Server"
            },
            {
               "value":"oracle",
               "text":"Oracle"
            },
            {
               "value":"aws_postgresql",
               "text":"AWS RDS for PostgreSQL"
            },
            {
               "value":"postgresql",
               "text":"PostgreSql"
            },
            {
               "value":"aws_mysql",
               "text":"AWS RDS for MySQL"
            },
            {
               "value":"mysql",
               "text":"MySql"
            },
            {
               "value":"mongodb",
               "text":"MongoDB"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer"
            }
         ],
         "required":false
      },
      {
         "id":"source_location",
         "order":33,
         "controlType":"dropdown",
         "visibility":"source_engine != aws_sql && source_engine != aws_postgresql && source_engine != aws_mysql",
         "displayLabel":"Where is located the database engine?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"azure",
               "text":"Azure"
            },
            {
               "value":"onpremises",
               "text":"On-premises"
            },
            {
               "value":"cloud",
               "text":"Other Cloud provider"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer"
            }
         ],
         "required":false
      },
      {
         "id":"type_activity",
         "order":35,
         "controlType":"dropdown",
         "visibility":"issue_type == migrating || issue_type == managing",
         "displayLabel":"What is the type of activity of the project?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"schema",
               "text":"Schema only migration"
            },
            {
               "value":"offline",
               "text":"Offline data migration"
            },
            {
               "value":"online",
               "text":"Online data migration"
            },
            {
               "value":"project",
               "text":"Create project only"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer"
            }
         ],
         "required":false
      },
      {
         "id":"dma",
         "order":40,
         "controlType":"dropdown",
         "visibility":"issue_type == migrating && source_engine == sql",
         "displayLabel":"Have you used Database Migration Assistant (DMA)?",
         "watermarkText":"Choose an option",
         "dropdownOptions":[
            {
               "value":"yes",
               "text":"Yes and it didn't found any compatibility issue"
            },
            {
               "value":"yes_resolver",
               "text":"Yes it has found issues that were fixed"
            },
            {
               "value":"yes_unresolved",
               "text":"Yes if was found issues that require support"
            },
            {
               "value":"no",
               "text":"No"
            },
            {
               "value":"running_issues",
               "text":"Can't run due to other issues"
            },
            {
               "value":"dont_know_answer",
               "text":"Don't know the answer"
            }
         ],
         "required":false
      },
      {
         "id":"problem_description",
         "order":99,
         "controlType":"multilinetextbox",
         "useAsAdditionalDetails":true,
         "displayLabel":"Details of the issue.",
         "watermarkText":"Please provide additional context for the error message you are encountering",
         "required":true
      }
   ]
}
---
