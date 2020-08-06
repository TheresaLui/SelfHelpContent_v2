<properties
	pageTitle="How to query/close handles using Azure Support Center(ASC)"
	description="How to query/close handles using Azure Support Center(ASC)"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="fda30f61-14ce-4a00-99d1-4350c22e91df"
/>

# How to query/close handles using Azure Support Center(ASC)

Below are the steps detailed on how to perform the query and closure of opened Handles using ASC.

1. Open **[ASC Resource Explorer](https://azuresupportcenter.msftcloudes.com/resourceExplorer)** and select the ***Storage Account*** involved.
2. Select the '*File*' tab and navigate to the '*Search File Handle*' subsection
3. Fill the Azure File Share, Directory or File path to search for the opened handles. Format: *{fileshare}/{file or directory path}*
4. Review the report of opened handles
5. **Ask for the customer consent** if any or all of the handles needs to be forcefully closed by Microsoft.
6. **Create ICM** with the details of the Handle/s to be closed and Storage Account information. **ICM Template**: [https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=RK24oB](https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=RK24oB)
7. **Follow the correct section below** whether you have access or not to the project [TM-CSSStgRec](https://myaccess/). **Note** that only TAs and several Storage SMEs have access to it.

**I have access to TM-CSSStgRec project**

1. Open the 'Force close handle' link in the ASC report or execute the Jarvis Action XStore-> Resource Property Retrieval -> [Force Close File Handle Operation](https://jarvis-west.dc.ad.msft.net/58B0211D?genevatraceguid=ecec0968-55a6-4621-bb0e-9d5c2baaf3e3)
2. Use the '**Get Access**' button to generate the JIT request
3. **Complete the JIT** request by filling the '*Work-item Id*' field with the previously created ICM, select the *Access Level* as **PlatformServiceOperator** and submit it. The other fields should auto-populate
4. Execute the query and validate with the customer
5. Resolve the ICM if issue is resolved

**I do not have access to TM-CSSStgRec project**

1. **Complete the below Template and send an email** with it to the global TA alias: **cssstgrec@microsoft.com** and **aivpta@microsoft.com** to help with the Force Close File Handle Operation.

~~~powershell

Force Close File Handles Template:
============
Case Number:
ICM Number: 
StorageAccountName: 
File Share or Path:
File Handle Id: 
Jarvis Action Query: Retrieve this value from "Force Close File" Handle link in ASC report

~~~
