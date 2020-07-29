<properties
	pageTitle="Perform verbose tracing"
	description="Perform verbose tracing"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="22c55743-ff8a-4a03-a98b-d43150404f5f"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Perform verbose tracing

* To perform verbose tracing, follow these steps

~~~powershell

Net Stop ADSync

~~~

* Open miiserver.exe.config
* Make sure folder c:\temp\ exists
* Add following fragment at appropriate location. 
*MAKE SURE YOUR EDITOR DIDN T INSERT NON ASCII CHARACTERS OR SPECIAL QUOTATION MARKS OR SPECIAL WHITESPACE CHARACTERS*

~~~xml

#JR needs to add this back

~~~

* Start ADSync

~~~powershell

Net Start ADSync 

~~~

* Run the experiment e.g. reset password on a test object and wait for 5-10 minutes, if running full password sync, wait for it to be over, or if you are troubleshooting connectivity issues etc, simply wait as necessary.
* Above configuration collects traces at C:\Temp\passwordSyncVerboseTrace.log
* Revert configuration to the original configuration when complete
* Send diagnostics collected to PG/EEE for analysis if nothing found on initial analysis
