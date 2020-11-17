<properties
	pageTitle="How to check for deletion details from ASC"
	description="How to check for deletion details from ASC"
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
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="deaa5095-2c36-4dc2-bfc1-1fadcc47a67c"
/>

# How to check for deletion details from ASC

1. Navigate to **Resource Explorer** and search for the affected Storage Account resource.
2. Select **Blob** tab/section.
3. Navigate to the subsection **Blob/Container Deletion Lookup & Recovery**
4. Click + **Get Deletion & Recovery Info** and fill the details of the deletion operation of the resource we are attempting to recover and **Run** the query.
5. Once status is **Succeeded**, review the Result and Recover Status

<br>
<br>

## How to check for deleted container name
<br>
KUSTO

Execute: [Web](https://dataexplorer.azure.com/clusters/disks.kusto.windows.net/databases/Disks?query=H4sIAAAAAAAEAG2PwWrDMAyG74G8g8klKYTCYLfRgdeGkUPT0qSnsYNiiTXDsYPssBX28HPTsW60N%2fHrs%2fz9mrxwY1uiWIjkpd4%2flavX5CGOdMhraaAnsQh5s9nJ50Iul5t91VRyXUyQ0qPzxFkK3A9sMZ3NETy04ChL5W69PWf1wVJrPwvjuSMXR1%2fi40BMYsukOkdN11PtoR%2fEo4A3m93d4%2bwCMTk7sqJgqKzx0Bn3IwwGb27P2pcLdiAG31lTndr8YglSKEnJCQzy76T8lVEecGbS0%2fMS8%2f%2b38j%2ffT%2fOofXMcQq5Aa%2bJykIghnipbRmLRHq9bIzkl4ugbx5XRG4oBAAA%3d) [Desktop](https://disks.kusto.windows.net/Disks?query=H4sIAAAAAAAEAG2PwWrDMAyG74G8g8klKYTCYLfRgdeGkUPT0qSnsYNiiTXDsYPssBX28HPTsW60N%2fHrs%2fz9mrxwY1uiWIjkpd4%2flavX5CGOdMhraaAnsQh5s9nJ50Iul5t91VRyXUyQ0qPzxFkK3A9sMZ3NETy04ChL5W69PWf1wVJrPwvjuSMXR1%2fi40BMYsukOkdN11PtoR%2fEo4A3m93d4%2bwCMTk7sqJgqKzx0Bn3IwwGb27P2pcLdiAG31lTndr8YglSKEnJCQzy76T8lVEecGbS0%2fMS8%2f%2b38j%2ffT%2fOofXMcQq5Aa%2bJykIghnipbRmLRHq9bIzkl4ugbx5XRG4oBAAA%3d&web=0) [Web (Lens)](https://lens.msftcloudes.com/v2/#/discover/query//results?datasource=(cluster:disks.kusto.windows.net,database:Disks,type:Kusto)&query=H4sIAAAAAAAEAG2PwWrDMAyG74G8g8klKYTCYLfRgdeGkUPT0qSnsYNiiTXDsYPssBX28HPTsW60N%2fHrs%2fz9mrxwY1uiWIjkpd4%2flavX5CGOdMhraaAnsQh5s9nJ50Iul5t91VRyXUyQ0qPzxFkK3A9sMZ3NETy04ChL5W69PWf1wVJrPwvjuSMXR1%2fi40BMYsukOkdN11PtoR%2fEo4A3m93d4%2bwCMTk7sqJgqKzx0Bn3IwwGb27P2pcLdiAG31lTndr8YglSKEnJCQzy76T8lVEecGbS0%2fMS8%2f%2b38j%2ffT%2fOofXMcQq5Aa%2bJykIghnipbRmLRHq9bIzkl4ugbx5XRG4oBAAA%3d&runquery=1) [Desktop (SAW)](https://disks.kusto.windows.net/Disks?query=H4sIAAAAAAAEAG2PwWrDMAyG74G8g8klKYTCYLfRgdeGkUPT0qSnsYNiiTXDsYPssBX28HPTsW60N%2fHrs%2fz9mrxwY1uiWIjkpd4%2flavX5CGOdMhraaAnsQh5s9nJ50Iul5t91VRyXUyQ0qPzxFkK3A9sMZ3NETy04ChL5W69PWf1wVJrPwvjuSMXR1%2fi40BMYsukOkdN11PtoR%2fEo4A3m93d4%2bwCMTk7sqJgqKzx0Bn3IwwGb27P2pcLdiAG31lTndr8YglSKEnJCQzy76T8lVEecGbS0%2fMS8%2f%2b38j%2ffT%2fOofXMcQq5Aa%2bJykIghnipbRmLRHq9bIzkl4ugbx5XRG4oBAAA%3d&saw=1) [https://disks.kusto.windows.net/Disks](https://disks.kusto.windows.net/Disks)
```kusto
let subId = "[SUBID]"; 
let SAname ="[STORAGEACCOUNTNAME]";
cluster('armprod').database('ARMProd').ShoeboxEntries 
| where PreciseTimeStamp > ago(14d) 
| where resourceId contains subId and resourceId contains SAname 
| where operationName contains "DELETE" and operationName contains "CONTAINER"
| project PreciseTimeStamp, correlationId, operationName, resourceId, resultType, callerIpAddress 
| order by PreciseTimeStamp asc 
```
<br>

Jarvis - [Sample JARVIS Query](https://jarvis-west.dc.ad.msft.net/48E114C0)


```Jarvis
Endpoint: Diagnostics PROD (for public Azure)
Namespace: Xstore
Events to search: DiagnosticAuditLog
Time range: MM/DD/YYYY
Scoping conditions: Tenant == [Stamp Name]
```
```
Filtering conditions
OwnerAccountName contains [STORAGE ACCOUNT NAME]
operationName == DeleteContainer
```
(you can use nslookup .blob.core.windows.net to determine tenant)