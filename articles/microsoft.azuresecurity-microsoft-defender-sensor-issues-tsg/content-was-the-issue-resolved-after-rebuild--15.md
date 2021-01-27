<properties
	  pageTitle="Was the issue resolved after rebuild?"
	  description="Was the issue resolved after rebuild?"
      service="Microsoft.Security"
      resource="Microsoft.Security/assessments"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="5dd7f9a2-9b83-4e50-b5eb-68ed54b37ad7"
	  ownershipId="Azure_Security_Security_Center"
/>

# Was the issue resolved after rebuild?

If the log inidcates the issue: 

~~~powershell

Warn PerformanceCounterMetricHelper PdhAddEnglishCounter failed.

~~~

See: [Rebuild Performance Counter Library values Windows Server](https://support.microsoft.com/help/300956/how-to-manually-rebuild-performance-counter-library-values?[pdhAddEnglishCounterResult=0xC0000BB8 SystemUpTime=23.21:28:25.1870000 FullName=\.NET CLR Memory%28Microsoft.Tri.Sensor.Updater%29\Promoted Memory from Gen 0 OperatingSystemFullName=\.NET CLR Memory%28Microsoft.Tri.Sensor.Updater%29\Promoted Memory from Gen 0])

This article describes how to manually rebuild Performance Counter Library values.

Another example of the log: 

~~~powershell

Error PerformanceCounterLib System.InvalidOperationException: Category does not exist.
at CategorySample System.Diagnostics.PerformanceCounterLib.GetCategorySample(string machine, string category) at string[] System.Diagnostics.PerformanceCounterCategory.GetCounterInstances(string categoryName, string machineName)at new Microsoft.Tri.Infrastructure.MetricManager(IConfigurationManager configurationManager)
at object lambda_method(Closure, object[] at object Autofac.Core.Activators.Reflection.ConstructorParameterBinding.Instantiate()
  at void Microsoft.Tri.Infrastructure.ModuleManager.AddModules(Type[] moduleTypes)
 at ModuleManager Microsoft.Tri.Sensor.Updater.SensorUpdaterService.CreateModuleManager()
  at async Task Microsoft.Tri.Infrastructure.Service.OnStartAsync()
 at void Microsoft.Tri.Infrastructure.TaskExtension.Await(Task task)
  at void Microsoft.Tri.Infrastructure.Service.OnStart(string[] args)

~~~

These type of logs are related to performance counter issues, it is recommended to follow the procedure below:

1. Check for "DisablePerformanceCounters" regkey, they should not exist or be set to '0':
    1. HKLM\System\CurrentControlSet\Services\PerfOS\Performance
    2. HKLM\System\CurrentControlSet\Services\PerfProc\Performance\
    3. HKLM\System\CurrentControlSet\Services\PerfNet\Performance\
2. Stop both MDI services
3. Rebuild counters with the following commands:
4. Rebuilding the counters, please use powershell or cmd prompt:
   1. cd c:\windows\system32 
   2. lodctr /R
   3. cd c:\windows\sysWOW64
   4. lodctr /R
4. Resyncing the counters with Windows Management Instrumentation (WMI):
   1. WINMGMT.EXE /RESYNCPERF
5. If the above doesn't resolve the issue please reboot the affected server 
