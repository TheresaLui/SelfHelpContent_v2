<properties
  pagetitle="Cannot start SQL Server Service "
  description="SQL Service startup or configuration"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740089"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="590dc858-f3e3-459e-9224-7100e0dff53d"
  ownershipid="AzureData_AzureSQLVM" />
# Cannot start SQL Server Service 

Most users can resolve issues with SQL Service by using the following steps. 

## **Recommended Steps** 

* **Can't start SQL Service or unexpected SQL Service shutdown** 

   * SQL Service doesn't start because of missing TempDB folders

     If you restarted or resized your VM, SQL Service may not start because of missing Tempdb files or folders on the D Drive. We're working on a fix for this. Meanwhile, run the following script, which creates the TempDB structure: 

      ``` 
      $SQLService="SQL Server (MSSQLSERVER)" 
      $SQLAgentService="SQL Server Agent (MSSQLSERVER)" 
      $tempfolder="D:\tempDB\Data" 
      $logfolder="D:\tempDB\Log" 
      if (!(test-path -path $tempfolder))  {   
      New-Item -ItemType directory -Path $logfolder   
      New-Item -ItemType directory -Path $tempfolder } 
      Start-Service $SQLService  
      Start-Service $SQLAgentService 
      ``` 
        
  *  **"Error: Could not open Data/Log file" or "OS error: 3 (The system cannot find the path specified.)"** 

    * Make sure your database files master, model, and `msdb` and `tempdb` files, which are required for starting SQL Server, are at the **correct location** and that **[SQL Service account has permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15#Windows) on the folders** where these files are stored. 

    * Check the SQL error log to determine if it contains anything related to the issue. See [SQL error log](https://docs.microsoft.com/sql/tools/configuration-manager/viewing-the-sql-server-error-log?view=sql-server-ver15). For SQL agent startup issues, check [SQL agent logs](https://docs.microsoft.com/sql/ssms/agent/sql-server-agent-error-log?view=sql-server-ver15). Are you able to [start the service from command prompt](https://docs.microsoft.com/sql/database-engine/configure-windows/start-stop-pause-resume-restart-sql-server-services?view=sql-server-ver15#CommandPrompt)? If the password has expired, change the SQL Server Service account. 

* **Can't log in to SQL Server** 

    * **Error: "Cannot Generate SSPI Context"** 
  
      To resolve this SPN issue, log in to the VM as Domain Admin and [run Kerberos Configuration Manager.](https://www.microsoft.com/download/details.aspx?id=39046).

   - To **reset your password**, [Add your own login/Reset SA Password](https://docs.microsoft.com/sql/database-engine/configure-windows/connect-to-sql-server-when-system-administrators-are-locked-out?view=sql-server-ver15#step-by-step-instructions). 

   - If your **password is expired** and **account is locked,** [change the password of a login](https://docs.microsoft.com/sql/t-sql/statements/alter-login-transact-sql?view=sql-server-ver15#b-changing-the-password-of-a-login).

* **IAAS Extension failed or SQL Virtual Machine Resource is unavailable** 

   Remove and [reinstall IAAS Agent Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-agent-extension-manually-register-single-vm?tabs=bash%2Cazure-cli).
 
* **SQL Server Configuration Manager** throws the error "Cannot Connect to WMI Provider. You do not have permission or the server is unreachable" 

   Check what version of SQL Server you have and replace it with the value `130`. You can try to repair this by compiling the `Mof` file by running the following in Command Prompt: 

   ``` 
   mofcomp "%programfiles(x86)%\\Microsoft SQL Server\\130\\Shared\\sqlmgmproviderxpsp2up.mof" 
  ``` 

## **Recommended Documents** 

* [Configure Service Accounts and Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15) 
* [Using GMSA Account](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831782(v=ws.11)) 
* [Change the SQL Language/Locale](https://techcommunity.microsoft.com/t5/sql-server-support/change-locale-language-of-sql-server-on-azure-vm/ba-p/1707566) 
* Mail alert has been received regarding scheduled activity from Microsoft to install [SQL IaaS Agent Extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-server-iaas-agent-extension-automate-management?tabs=azure-powershell) on VM which has no impact and will not cause any downtime
