<properties
	pageTitle="error connecting to Kubernetes cluster"
	description="error connecting to Kubernetes cluster"
	infoBubbleText="error connecting to Kubernetes cluster"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="0e7c70e6-e69c-4826-b5e7-dc40cd58c055"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747903"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
	
# Connecting Kubernetes with the machine where PostgreSQL Hyperscale Server Group Azure Arc is installed

Most users are able to resolve their issues related  to connectivity to the Kubernetes cluster using the recommended steps below.

## **Recommended Steps**

* Validate the namespace you are connecting to by using the following sample commands:

   ```bash
   kubectl get namespace
   kubectl get pods -n arc_namespace
   ```

* Make sure kubernetes and  Container engine (e.g. Docker) are running. Restart if needed and if possible.

   ```bash
   systemctl status docker
   systemctl status kubelet
   ```

* Check for Firewall blocking any ports. The following sample commands will list firewall access and status on Ubuntu systems.

   ```bash
   sudo iptables -L
   sudo ufw status
   ```

* Show the cluster endpoint and port your client (e.g. kubectl) is configured to connect to by using the following command.

   ```bash
   kubectl config view
   kubectl config view -o jsonpath='{"Cluster name\tServer\n"}{range .clusters[*]}{.name}{"\t"}{.cluster.server}{"\n"}{end}'
   ```
  
   Sample output may look like this:

   ```bash
   Cluster name    Server
   kubernetes      https://172.29.14.10:6443
   ```

    * Using the kubernetes server endpoint, test connectivity via **telnet**

        ```bash
        telnet 172.29.14.05 6443
        ```

    * If port is open (not blocked) and IP address valid, you should receive a result similar to this:

   ```bash
   Trying 172.29.14.05...
   Connected to 172.29.14.05.
   Escape character is '^]'.
   CTRL+]
   telnet> quit
   ```

* If you are able to connect to a cluster but you are not getting the expected results, list the Azure Arc endpoints and make sure you are connected to the right Azure Arc Controller endpoint

   ```bash
   azdata arc dc endpoint list
   ```

* If you are not able to run any azdata commands, but kubectl commands work, have you ensured that you have logged into the Data Controller?

   ```bash
   Azdata login
   ```

## **Recommended Documents**

- [Accessing Clusters](https://kubernetes.io/docs/tasks/access-application-cluster/access-cluster/)
- [Access Clusters Using the Kubernetes API](https://kubernetes.io/docs/tasks/administer-cluster/access-cluster-api/)