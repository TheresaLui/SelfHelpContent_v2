<properties
	pageTitle="Investigate high CPU using azprofiler"
	description="Investigate high CPU using azprofiler"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c25f8a0f-a7fc-47ca-b17b-675539b8921c"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Investigate high CPU using azprofiler

1. Use [Azure Profile viewer](http://azprofilerclko) to deeper investigate high host CPU issues by using the following options
2. Look for "Azure Profiler" tab in Hostanalyzer Report below tab "Host Metrics"
3. Do the following manual steps:
    1. Open Azure Profile viewer and select "View Data from Specific Compute Hosts"
	2. Select "NodeHighCPU"
	3. Then select Year, Month and Day that corresponds to the incident.
    4. Provide the HOSTS name have to be provided to search for the trace
	5. The host name can be seen within the host CPU chart
	6. Within the trace double click the orange bar to see the defailts of the call stack
4. The call stack information can be used to address the right PG team who owns the components within the calls stack. If High Host CPU seem to have impacted VM availability (e.g. by causing an E17), please open an ICM to EEE.
5. You may also check Kusto for a log of high host CPU events
    1. Kusto query to check for High Host CPU events (which will also be shown in Hostanalyzer in tab "Host Metrics"/"High CPU Node Table"):
	2. [Kusto Instance](https://vmainsight.kusto.windows.net/vmadb)

~~~kusto

 HighCpuCounterNodeTable
    | where NodeId == "<NodeID>"
    | where PreciseTimeStamp >  datetime(<StartTime>)
    | where PreciseTimeStamp < datetime(<EndTime>)

~~~
