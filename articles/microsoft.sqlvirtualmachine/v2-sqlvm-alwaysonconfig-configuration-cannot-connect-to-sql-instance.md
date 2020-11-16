<properties
	pageTitle="Cannot Connect to SQL instance"
	description="Cannot Connect to SQL instance"
	infoBubbleText="Cannot Connect to SQL instance"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740109"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="a3d57b5a-47b5-4116-adf7-2840660b4fdb"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you.


<!--issueDescription--> 

4 out of 5 customers are able to resolve their **SQL Connectivity issues** using the recommended documents below.   

<!--/issueDescription--> 

## **Recommended Steps** 

 

- **Most Common Errors** 

 

  * **Error:"Cannot Generate SSPI Context"** while connecting to SQL Server 

 

    Connectivity to SQL May fail because of SPN duplication, Incorrectly registered or missing entries. Download,Login in the VM as **Domain Administrator** and [Run Kerberos Configuration Manager](https://www.microsoft.com/download/details.aspx?id=39046) to fix these SPN issues. 

 

  * **SQL Service does not Start because of Missing TempDB Folders** 

 

     If you restarted your VM or Resized your VM, SQL May not start because of Tempdb Files/Folders missing on the D Drive. We are working on a fix for this. Please run the below script to Resolve this which creates the TempDB structure: 

    ```PS 
      $SQLService="SQL Server (MSSQLSERVER)" 
      $SQLAgentService="SQL Server Agent (MSSQLSERVER)" 
      $tempfolder="D:\tempDB\Data" 
      $logfolder="D:\tempDB\Log" 
      if (!(test-path -path $tempfolder)) 
       {     
       New-Item -ItemType directory -Path $logfolder   
       New-Item -ItemType directory -Path $tempfolder 
       } 
       Start-Service $SQLService  
       Start-Service $SQLAgentService 
      ```` 
   * **Seeing Login Failures for Account "NT SERVICE\\SqlIaaSExtensionQuery".** 

     Uninstall and [Reinstalling Resource Provider](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=bash%2Cazure-cli#lightweight-management-mode) can fix the issue. Installing of Fullweight Management Mode for Resource provider requires a SQL Service Restart. Make sure you have this as a login in your SQL Server or run: 

     ```SQL 
      CREATE LOGIN [NT Service\SQLIaaSExtensionQuery] FROM WINDOWS WITH DEFAULT_DATABASE=[master] 
      GO 
      ALTER SERVER ROLE [sysadmin] ADD MEMBER [NT Service\SQLIaaSExtensionQuery] 
      GO 
      ``` 

 

  *   **Azure Active Directory authentication/connectivity is not supported with Azure SQL VM** 

 

      SQL Server on Azure VM supports Windows Authentication and SQL Authentication. [Review this Document]( https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-overview) 

 

   * **I forgot sysadmin (sa) password, how do I login to SQL Server Instance**  

     To gain access to SQL Server, run the below command in command prompt with Administrator Privilege's. Replace Domain\login with your domain and user that you want: 

     ```SQL     
      NET STOP MSSQLSERVER 
      NET START MSSQLSERVER /m"SQLCMD" 
      sqlcmd -S MY_SERVER_NAME 
      CREATE LOGIN [Domain\login] FROM WINDOWS;  
      GO 
      ALTER SERVER ROLE sysadmin ADD MEMBER [Domain\login]; 
      Go 
      Exit 
      NET STOP MSSQLSERVER 
      NET start MSSQLSERVER 
     ``` 

 

- **90% of SQL instance connectivity Issues are resolved by following the below Diagnose and Mitigate action Steps** 

    * If you are having issues connecting to SQL Server Instance on Azure VM from a different Network or On-Prem, Please [Review this Document](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/ways-to-connect-to-sql) 

   * Make Sure Port used by SQL Server (1433) is open for inbound/outbound connections and You can [Telnet](https://docs.microsoft.com/windows-server/administration/windows-commands/telnet) to the Port or use [Test-NetConnection](https://docs.microsoft.com/powershell/module/nettcpip/test-netconnection?view=win10-ps#example-3--test-tcp-connectivity-and-display-detailed-results) to check if its blocked at **NSG or Windows Firewall**. Make sure your company firewall is not blocking these connections(Check with your **Network Admin**). An outbound rule from where you make a connection has to be added for the SQL Port to Windows Firewall and Company Firewall.   


  * Make sure TCP/IP and shared memory in [SQL server configuration are Enabled](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-or-disable-a-server-network-protocol?view=sql-server-ver15#SSMSProcedure) 
 
  * You may see intermittent connectivity issues to SQL instance if your AG Failed over or if you are having AG [Lease Timeout](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/availability-group-lease-healthcheck-timeout?view=sql-server-ver15#updating-cluster-and-always-on-timeout-values) or if you are having issues with [SQL Performance](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices), Network issues or [Disk or VM Throttling](https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics). Check SQL Error log to find out more. 


## **Recommended Documents**

* [Solving Connectivity errors to SQL Server](https://support.microsoft.com/help/4009936/solving-connectivity-errors-to-sql-server)
* [Applications experience forcibly closed TLS connection errors](https://docs.microsoft.com/troubleshoot/windows-server/identity/apps-forcibly-closed-tls-connection-errors)
* [Connect to a SQL Server Virtual Machine on Azure VM](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/ways-to-connect-to-sql)
* [SQL Server connectivity drivers](https://msdn.microsoft.com/library/mt654049.aspx)
* [Upgrade to TLS 1.2 for Secure Communication](https://support.microsoft.com/help/3135244/kb3135244-tls-1-2-support-for-microsoft-sql-server)
 
