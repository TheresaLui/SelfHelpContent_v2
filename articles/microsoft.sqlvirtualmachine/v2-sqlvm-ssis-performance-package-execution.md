<properties
  pagetitle="Issue in performance of package execution"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="hecepeda"
  selfhelptype="Generic"
  supporttopicids="32749437"
  resourcetags=""
  productpesids="14745"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  disableclouds=""
  articleid="sqlvm-ssis-performance-package-execution"
  ownershipid="AzureData_AzureSQLVM" />

# **Issue in performance of package execution**

Please note that typically for SSIS performance issues, you will not receive any specific error messages. The user might report an issue that their package execution is taking longer time to complete, or it is slow or it has hung for long time and at the same time the CPU and memory is taking higher value than normal.

However, there could be some execution failures with the below error messages reported.

**Errors:**

```
Description: The input buffer could not be cloned. An out-of-memory condition...

Error : An OLE DB record is available. Source: "Microsoft Cursor Engine" Hresult: 0x8007000E Description: "Out of memory.".

Error: The Data Flow task failed to create a buffer to call PrimeOutput for output "YYYYY" (n) on component "XXXX". This error usually occurs due to an out-of-memory condition.
```

If you are receiving an _out-of-memory_ message, check if you are executing the SSIS package under **32bit** execution runtime. If so, please verify if they can be executed under **64bit** runtime by removing any dependencies. By executing the SSIS packages under **32bit** runtime, we can very easily hit the **2 GB limit**. The 2 GB limit for 32bit process is not a limitation for SSIS execution process alone, rather it is applicable to all 32bit process. It is applicable to any 32bit process on 64bit OS as well.

Read this article, which talks about this in detail [https://docs.microsoft.com/troubleshoot/aspnet/troubleshoot-outofmemoryexception](https://docs.microsoft.com/troubleshoot/aspnet/troubleshoot-outofmemoryexception)

SSIS is an in-memory process. It uses the primary memory (RAM) to store the data while it is doing any ETL operation. So, we need to check if it reaches the memory threshold. If it does reach the memory threshold, then we may need to scale up the server (**add more physical memory – RAM**) to avoid these error messages.

**Errors:**

```
Error: The buffer manager failed a memory allocation call for XXXX bytes, but was unable to swap out any buffers to relieve memory pressure. XXX buffers were considered and XXX were locked. Either not enough memory is available to the pipeline because not enough are installed, other processes were using it, or too many buffers are locked.

Error: A buffer failed while allocating XXXX bytes.

Error : The attempt to add a row to the Data Flow task buffer failed with error code 0xC0047020
```

You will receive the above error messages when the SSIS memory manager fails to allocate a pipeline buffer due to low system virtual memory. Please make sure that the system has enough available memory to complete the operation.

In case of packages taking longer time to complete than what is expected, we need to investigate this both from the execution environment perspective as well as the design of the package.

From execution environment standpoint, please review your server machine during the time of package execution to understand if there are any other applications / processes that are consuming most of the available physical memory in the machine (like SQL Server process 'sqlsrvr.exe') and thus stalling the SSIS execution. If so, please review and correct this high memory consuming application. (like capping memory)

From package design perspective, we need to start with understanding the design of the package, and which component is taking longer amount of time. To do so, we need to collect the execution or performance log for the package and check for the components consuming higher time for completion.

You can review the below documentation for enhancing your package design.

## **Recommended Documents**

[Data Flow Performance Features](https://docs.microsoft.com/sql/integration-services/data-flow/data-flow-performance-features?view=sql-server-ver15)
