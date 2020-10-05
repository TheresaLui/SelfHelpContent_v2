<properties
	pageTitle="Create PostgreSQL Hyperscale Server group"
	description="Create PostgreSQL Hyperscale Server group"
	infoBubbleText="Create PostgreSQL Hyperscale Server group"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="e3c22dd9-bead-4723-85ac-929a33e6b0d3"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747900"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
	
# Create PostgreSQL Hyperscale Azure Arc resource

Most users are able to resolve their issues with creating or deploying a PostgreSQL Hyperscale Azure Arc using the recommended steps below.

## **Recommended Steps**

* Ensure you are following the pre-requisites mentioned in [Create an Azure Arc enabled PostgreSQL Hyperscale server group](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group)
* If you are using Open shift ensure that you have read [Preliminary and temporary step for OpenShift users only](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group#preliminary-and-temporary-step-for-openshift-users-only)
* If you have issues during the installation troubleshoot using the steps below

### Commands useful for troubleshooting PostgreSQL Hyperscale server group creation issues

* You can use the **--debug** switch to get verbose information about the progress of your deployment. For example: 

   ```bash
   azdata arc postgres server create -n postgres01 --workers 2 --debug
   ```
   
* After completion of a Postgres-instance creation examine the **azdata.log**:
 
   ```bash
   tail -f ~/.azdata/logs/azdata.log   #(ctrl+C to stop monitoring)
   tail -n 200  ~/.azdata/logs/azdata.log
   ```

* Examine one or more Pods to see if you can find the answers there. Look at the pod STATUS and see if it is anything other than *Running*. Also look at the Ready column and see how many of the pods are in the state (e.g. 2/3 means two of the three pods are ready and available). Then you can describe a pod that is not in a *Running* state. Pay special attention to the Events at the very end of the **kubectl describe** output:

   ```bash
   kubectl get pods 
   kubectl describe pod <pod> -n <namespace>
   ```

* If you discover a particular pod is the source of causing the issues, examine any logs exposed by specific containers in that pod using **kubectl logs -c <container_of_interest> <pod_of_interest>**:

   ```bash
   kubectl logs -c postgres01 postgres01-0
   ```

* You can monitor the Linux system log live or you can examine it after the completion of a postgres server group creation:

   ```bash
   tail -f /var/log/syslog
   tail -n 200 /var/log/syslog
   ```

* If no obvious issues are found in postgres server group pods, or if you cannot find a clear reason there, examine the Kubernetes events for possible root cause:

   ```bash
   kubectl get events -n kube-system
   kubectl get events -n <arc namespace>
   ```

* You can also examine Docker container state and docker logs for possible issue with Docker itself. First find the running containers and pick a name using docker ps. Then examine the logs for that container using **docker logs <cotainer>**. For example:

   ```bash
   docker ps  
   docker logs k8s_kibana_logsui-xl8qw_arc_6f74c04f-e1ea-47f1-924e-0ff971ef6981_2
   ```		 

## **Recommended Documents**

- [Create an Azure Arc enabled PostgreSQL Hyperscale server group](https://docs.microsoft.com/azure/azure-arc/data/create-postgresql-hyperscale-server-group)
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
- [Show configuration of a server group](https://docs.microsoft.com/azure/azure-arc/data/show-configuration-postgresql-hyperscale-server-group)
- [Scale up/down (increase/decrease memory/vcore) a server group](https://docs.microsoft.com/azure/azure-arc/data/scale-up-down-postgresql-hyperscale-server-group-using-cli)
- [Scale out (add worker nodes)](https://docs.microsoft.com/azure/azure-arc/data/scale-out-postgresql-hyperscale-server-group)
- [Configure the Postgres database engine server parameters](https://docs.microsoft.com/azure/azure-arc/data/configure-server-parameters-postgresql-hyperscale)