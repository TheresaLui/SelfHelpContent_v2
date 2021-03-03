<properties
	pageTitle="General Performance Troubleshooting"
	description="General Performance Troubleshooting"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="f0fa589b-2e27-4e39-a4e7-9689b85d3feb"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# General Performance Troubleshooting

**IMPORTANT:** Before attempting to diagnose performance issues from the log files, try using AzCopy's [benchmark mode](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=use-benchmark-feature-to-troubleshoot-performance-issues). It will conduct diagnostic tests for you, and report on most common performance issues automatically.

When searching AzCopy log files, it is advisable to use **grep** (if on **Linux**) or **select-string** (if in **PowerShell** on **Windows**). For large log files, that?s much more practical that trying to open the whole file in a text editor. For example, in PowerShell here?s how to extract all the performance information from a log file into a separate file named perfLines.txt

~~~log

select-string PERF .\858ebb30-4796-914f-632e-dc355cda0e1c.log | Out-File perfLines.txt

~~~

The Linux equivalent is: 

~~~shell

grep PERF ./858ebb30-4796-914f-632e-dc355cda0e1c.log > perfLines.txt

~~~

The performance log looks like:

~~~log

858ebb30-4796-914f-632e-dc355cda0e1c.log:94549:2019/04/03 06:42:16 PERF: primary performance constraint is Unknown. States: R: 0, D: 289, W: 1046, F: 0, B: 12, T: 1347

~~~

The section that says **primary performance constraint is** corresponds to the messages described above. It may say that the primary constraint is:
1. Disk (this is what gets logged when the screen says ?Disk may be limiting speed?)
2. PageBlobService (this get logged when the screen says ?PageBlobService may be limiting speed?)
3. Service (this get logged when the screen says ?Service may be limiting speed?)
4. Unknown. This is logged in all other cases. i.e. when there is no limit message on screen.
5. When it says ?Unknown? that doesn?t mean that there is nothing limiting throughput (there?s always something). It just means that AzCopy hasn?t figured out exactly what the constraint is. Possible constraints included: [**Here**](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=troubleshooting-azcopy-performance-issues)
