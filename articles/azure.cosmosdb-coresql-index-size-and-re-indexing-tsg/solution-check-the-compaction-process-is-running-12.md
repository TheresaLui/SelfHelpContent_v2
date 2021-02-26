<properties
	  pageTitle="Check the compaction process is running"
	  description="Check the compaction process is running"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="a8cf3051-6427-420b-a4d1-fc77e71eb302"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check the compaction process is running

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 

1. The compaction is executed on each partition. 
2. Extract any partition ID for a given collection and replace predicate value below.

```
ReplicaCounterFiveMinute
| where CounterName contains 'd808b694-d79a-45ab-bf7c-f536ea204aef' //partition id
| where CounterName contains "BwTree"
| where CounterName contains 'compaction iO'
| where MaxCounterValue > 0
| project TIMESTAMP, CounterName, MaxCounterValue
```

3. The output should look like below or the Chart should be like given below. Then the compaction is running which means the space is continuously released.

```
TIMESTAMP	CounterName	       MaxCounterValue
2020-02-19 15:40:00.0000000	\DocDB Server Replica Counters(16464P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132118462240642307_Fri, 07 Feb 2020 23:52:11.315 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	46.0116515305171
2020-02-19 15:50:00.0000000	\DocDB Server Replica Counters(2764P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132231579243949858_Sat, 08 Feb 2020 15:29:43.133 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	10.0030893207622
2020-02-19 16:05:00.0000000	\DocDB Server Replica Counters(2764P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132231579243949858_Sat, 08 Feb 2020 15:29:43.133 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	11.084959351842
2020-02-19 16:40:00.0000000	\DocDB Server Replica Counters(12984P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132255492390961260_Sat, 08 Feb 2020 15:06:36.110 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	21.764133321548
2020-02-19 17:20:00.0000000	\DocDB Server Replica Counters(12984P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132255492390961260_Sat, 08 Feb 2020 15:06:36.110 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	36.8698068129743
2020-02-19 17:20:00.0000000	\DocDB Server Replica Counters(16464P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132118462240642307_Fri, 07 Feb 2020 23:52:11.315 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	18.3666466470218
2020-02-19 17:25:00.0000000	\DocDB Server Replica Counters(11512P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132158145462074212_Sat, 08 Feb 2020 14:02:24.332 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	34.9226561067568
2020-02-19 17:35:00.0000000	\DocDB Server Replica Counters(16464P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132118462240642307_Fri, 07 Feb 2020 23:52:11.315 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	30.0569826887202
2020-02-19 18:00:00.0000000	\DocDB Server Replica Counters(16464P_d808b694-d79a-45ab-bf7c-f536ea204aef_R_132118462240642307_Fri, 07 Feb 2020 23:52:11.315 GMT)   \BwTree Background Compaction IO Reads/sec (Consistent)	20.1330075050146
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query.

<!--/issueDescription-->

