<properties
      pageTitle="GuestAgentPluginInstallCommandProcessingFailed"
      description="GuestAgentPluginInstallCommandProcessingFailed"
      infoBubbleText="Extension failed to due to run time environment failure"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-guestagentplugininstallcommandprocessingfailed"
      diagnosticScenario="azurebackup-crc-guestagentplugininstallcommandprocessingfailed"
      selfHelpType="diagnostics"
      supportTopicIds=""
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# GuestAgentPluginInstallCommandProcessingFailed

<!--issueDescription-->
Extension failed to start. This can be due to runtime environment failure.
<!--/issueDescription-->

To resolve this issue: 
- Ensure that the latest [.NET is installed](https://docs.microsoft.com/dotnet/framework/install/) and running on the Windows VM 
- Ensure that Python 2.7 is installed on Linux VM and check if the [Linux Operating system meets the OS requirements](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
