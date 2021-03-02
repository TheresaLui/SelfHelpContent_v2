<properties
    pageTitle="performance/blocking sessions"
    description="performance/blocking sessions"
    infoBubbleText="Found blocking sessions on this database. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="Blocking_9E96233D-12F4-4CF7-9F4C-98301A27784F"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749512,32749515,32749520,32749519"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="Public,Mooncake,fairfax,usnat,ussec"
    ownershipId="AzureData_AzureSQLDB_Performance"
/>

# We ran diagnostics on your database and found blocking sessions.

<!--issueDescription-->
Our internal service telemetry detected blocking sessions on the database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on the server **<!--$ServerName-->ServerName<!--/$ServerName-->** between **<!--$StartTime-->StartTime<!--/$StartTime--> UTC** and **<!--$EndTime-->EndTime<!--/$EndTime--> UTC**. 
We have identified at least one lead blocking session.

Blocking occurs when one session holds a lock on a specific resource and a second session attempts to acquire a conflicting lock type on the same resource. When locking and blocking persists, it can have detrimental effect on system performance.
<!--/issueDescription-->

## **Recommended Steps**
We recommend running the query below to identify the lead blocking session. 

1. Check the `wait_duration_ms` to determine if the blocking is impactful.

2. Run the following query:

   ```sql

   WITH cteHead ( session_id,request_id,wait_type,wait_resource,last_wait_type,is_user_process,request_cpu_time
   ,request_logical_reads,request_reads,request_writes,wait_time,blocking_session_id,memory_usage
   ,session_cpu_time,session_reads,session_writes,session_logical_reads
   ,percent_complete,est_completion_time,request_start_time,request_status,command
   ,plan_handle,sql_handle,statement_start_offset,statement_end_offset,most_recent_sql_handle
   ,session_status,group_id,query_hash,query_plan_hash)
   AS ( SELECT sess.session_id, req.request_id, LEFT (ISNULL (req.wait_type, ''), 50) AS 'wait_type'
       , LEFT (ISNULL (req.wait_resource, ''), 40) AS 'wait_resource', LEFT (req.last_wait_type, 50) AS 'last_wait_type'
       , sess.is_user_process, req.cpu_time AS 'request_cpu_time', req.logical_reads AS 'request_logical_reads'
       , req.reads AS 'request_reads', req.writes AS 'request_writes', req.wait_time, req.blocking_session_id,sess.memory_usage
       , sess.cpu_time AS 'session_cpu_time', sess.reads AS 'session_reads', sess.writes AS 'session_writes', sess.logical_reads AS 'session_logical_reads'
       , CONVERT (decimal(5,2), req.percent_complete) AS 'percent_complete', req.estimated_completion_time AS 'est_completion_time'
       , req.start_time AS 'request_start_time', LEFT (req.status, 15) AS 'request_status', req.command
       , req.plan_handle, req.[sql_handle], req.statement_start_offset, req.statement_end_offset, conn.most_recent_sql_handle
       , LEFT (sess.status, 15) AS 'session_status', sess.group_id, req.query_hash, req.query_plan_hash
       FROM sys.dm_exec_sessions AS sess
       LEFT OUTER JOIN sys.dm_exec_requests AS req ON sess.session_id = req.session_id
       LEFT OUTER JOIN sys.dm_exec_connections AS conn on conn.session_id = sess.session_id
       )
   , cteBlockingHierarchy (head_blocker_session_id, session_id, blocking_session_id, wait_type, wait_duration_ms,
   wait_resource, statement_start_offset, statement_end_offset, plan_handle, sql_handle, most_recent_sql_handle, [Level])
   AS ( SELECT head.session_id AS head_blocker_session_id, head.session_id AS session_id, head.blocking_session_id
       , head.wait_type, head.wait_time, head.wait_resource, head.statement_start_offset, head.statement_end_offset
       , head.plan_handle, head.sql_handle, head.most_recent_sql_handle, 0 AS [Level]
       FROM cteHead AS head
       WHERE (head.blocking_session_id IS NULL OR head.blocking_session_id = 0)
       AND head.session_id IN (SELECT DISTINCT blocking_session_id FROM cteHead WHERE blocking_session_id != 0)
       UNION ALL
       SELECT h.head_blocker_session_id, blocked.session_id, blocked.blocking_session_id, blocked.wait_type,
       blocked.wait_time, blocked.wait_resource, h.statement_start_offset, h.statement_end_offset,
       h.plan_handle, h.sql_handle, h.most_recent_sql_handle, [Level] + 1
       FROM cteHead AS blocked
       INNER JOIN cteBlockingHierarchy AS h ON h.session_id = blocked.blocking_session_id and h.session_id!=blocked.session_id --avoid infinite recursion for latch type of    blocking
       WHERE h.wait_type COLLATE Latin1_General_BIN NOT IN ('EXCHANGE', 'CXPACKET') or h.wait_type is null
       )
   SELECT bh.*, txt.text AS blocker_query_or_most_recent_query
   FROM cteBlockingHierarchy AS bh
   OUTER APPLY sys.dm_exec_sql_text (ISNULL ([sql_handle], most_recent_sql_handle)) AS txt
   ORDER BY bh.wait_duration_ms DESC;

   ```
   
3. Do one of the following:
   -   If the query returns results, blocking is currently occurring. If the blocking is impacting workload performance, run the following command to kill the lead   blocker: 
       `KILL {head_blocker_session_id};` 
   -   If the query does not return results, blocking is not currently occurring. In this case, if you are still experiencing performance issues, review this article to help [identify other query performance issues in Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/identify-query-performance-issues).

3. Review [Understand and Resolve Azure SQL DB Blocking Problems](https://docs.microsoft.com/azure/azure-sql/database/understand-resolve-blocking) for more information.
