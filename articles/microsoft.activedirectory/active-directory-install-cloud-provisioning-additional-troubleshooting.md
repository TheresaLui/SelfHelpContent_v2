<properties
	pageTitle="Debugging using detailed logs emitted by Cloud Provisioning Agent"
	description="Debugging using detailed logs emitted by Cloud Provisioning Agent"
	infoBubbleText="Debugging using detailed logs emitted by Cloud Provisioning Agent"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	ms.author="Dhanyahk"
	displayOrder="2226"
	articleId="5989dcdf-d82b-4a9f-9c73-29d7913f6bc8"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32689667"
	resourceTags="directory_ad_connect"
	productPesIds="16666"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureIdentity_User"
/>

# Debugging advanced installation issues of cloud provisioning agent

You want to get advanced trace logs in order to debug agent installation issues.

## **Recommended Steps**

By default, the agent emits minimal error messages and stack trace information. You can find these trace logs in the folder <i>C:\ProgramData\Microsoft\Azure AD Connect Provisioning Agent\Trace.</i>

To gather additional details for troubleshooting agent-related problems, follow these steps:

1. Stop the service Microsoft Azure AD Connect Provisioning Agent
2. Create a copy of the original config file: <i>C:\Program Files\Microsoft Azure AD Connect Provisioning Agent\AADConnectProvisioningAgent.exe.config</i>
3. Replace the existing <system.diagnostics> section with the following, and all trace messages will go to the file ProvAgentTrace.log:

 ```
 <system.diagnostics>
       <sources>
       <source name="AAD Connect Provisioning Agent">
           <listeners>
           <add name="console"/>
           <add name="etw"/>
           <add name="textWriterListener"/>
           </listeners>
       </source>
       </sources>
       <sharedListeners>
       <add name="console" type="System.Diagnostics.ConsoleTraceListener" initializeData="false"/>
       <add name="etw" type="System.Diagnostics.EventLogTraceListener" initializeData="Azure AD Connect Provisioning Agent">
          <filter type="System.Diagnostics.EventTypeFilter" initializeData="All"/>
       </add>
       <add name="textWriterListener" type="System.Diagnostics.TextWriterTraceListener" initializeData="C:/ProgramData/Microsoft/Azure AD Connect Provisioning Agent/Trace/ProvAgentTrace.log"/>
       </sharedListeners>
   </system.diagnostics>
 ```
4. Start the service Microsoft Azure AD Connect Provisioning Agent
5. Use the following to view the log: `Get-Content "C:/ProgramData/Microsoft/Azure AD Connect Provisioning Agent/Trace/ProvAgentTrace.log" -Wait`

## **Recommended Documents**

* [Troubleshooting additional agent install issues](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#agent-problems)
* [Troubleshooting object synchronization issues](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#object-synchronization-problems)
* [Troubleshooting sync runs that are in quarantine](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#provisioning-quarantined-problems)
