<properties
	pageTitle="Gremlin Connectivity"
	description="Article explains how to troubleshoot gremlin connectivity issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32681008"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-gremlin-connectivity"
	displayOrder="188"
	category="Gremlin (Graph)"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Connectivity Issues
Most users are able to resolve their Cosmos DB Gremlin connectivity issues using the steps below.  


## **Recommended Steps**

### **Gremlin.Net.Driver.Exceptions.ServerUnavailableException:**
* If you are failing to connect and receiving a *Gremlin.Net.Driver.Exceptions.ServerUnavailableException* repeatedly, you may be using an older version of Gremlin Client (for example, 3.4.0.0).  

**Solution:** Upgrading to Gremlin .NET 3.4.2 or greater would probably resolve this issue. 

### **404 (NotFound) status code. NotFoundException**
* Compute layer caches the storage client by the collection name (e.g. "testGraph"). The cached client, however, identifies the collection by its resource id *rid*. This can result in compute requests that are issued after a collection recreate trying to use a cached client with the deleted collection's Rid. The storage layer cannot find the deleted collection, so returns a 404 (NotFound) status code. We forward this status code to the user, resulting in the observed NotFoundException.  

**Solution:** Please cycle the collection name when deleting and re-creating a collection (e.g. "testGraph1", "testGraph2", "testGraph3", . . . ).  

### **Date header doesn't conform to the required format**
* The Cosmos DB SDK has a dependency on joda-time lib 2.9.9.  Reference the Maven Artifact: [Java SDK for SQL API of Microsoft Azure Cosmos DB](https://mvnrepository.com/artifact/com.microsoft.azure/azure-documentdb/2.4.4). 
* If you are using an older version of joda-time < 2.9.9 (maybe as a transitive dependency by another dependency) You may encounter this issue.  

**Solution:** Verify you are using the correct version of joda-time and explicitly setting the dependency for joda-time 2.9.9 will resolve the issue  

### **Other Common Connectivity problems**
Open source Gremlin client drivers were initially designed to connect with individual servers. When they encounter a connectivity issues they mark the server as unavailable internally. This behavior presents a problem for Cosmos DB Graph database because behind a single host name your account.gremlin.cosmos.azure.com there is a virtual IP address of a load balancer that routes traffic within a cluster of computers. Connectivity failure to a single node in the cluster should not render entire VIP unavailable, but it does, for Gremlin client drivers.  

**Manifestations of this problem:**  
* .NET: **Gremlin.Net.Driver.Exceptions.ServerUnavailableException:** No connection to the server available which most likely means that the server is completely unavailable.
* .Java: **TimeoutException:** Timed-out waiting for connection on your account.gremlin.cosmos.azure.com - possibly unavailable.

**Connection Termination:**
* Connection was idle for over an hour and there was no traffic on it other than keep-alive messages. To reclaim resources Cosmos DB will close such connections.  
* Upgrade of Cosmos DB Graph database. Upgrade is rolling through the cluster and customer may experience intermittent connection failures as nodes are shut down and brought back up.
* Firewall rules, IP filter or VNET configuration on account was changed. In this event Cosmos DB Graph will terminate connections that are no longer allowed under new configuration.  

**Solution:** Whenever client application encounters connection failure the right course of action is to retry. At no point in time is the entire Cosmos DB Graph cluster down so retrying a failed connection is the recommended action.

For **Java** clients, it is recommended to override the default retry strategy with a custom one. This custom strategy should avoid invalidating a host when a single connection fails.

```
import java.util.Collection;
import java.util.Iterator;
import java.util.Random;
import java.util.concurrent.CopyOnWriteArrayList;
import java.util.concurrent.atomic.AtomicInteger;

import org.apache.tinkerpop.gremlin.driver.Cluster;
import org.apache.tinkerpop.gremlin.driver.Host;
import org.apache.tinkerpop.gremlin.driver.LoadBalancingStrategy;
import org.apache.tinkerpop.gremlin.driver.message.RequestMessage;

/**
 * This is a slightly modified version of default load balancing strategy 
 * from TinkerPop Gremlin Java Driver 
 * https://github.com/apache/tinkerpop/blob/master/gremlin-driver/src/main/java/org/apache/tinkerpop/gremlin/driver/LoadBalancingStrategy.java
 * 
 * In Microsoft Azure Cosmos DB there is only a single host (DNS CNAME) that
 * points to a single VIP behind which there are many physical nodes serving
 * traffic. It is incorrect to mark host as unavailable and look for a better
 * one because there won't be a better one. VIP does not go down, but a single
 * node can. Failure of a node should not render entire cluster unusable.
 * 
 * * @author Microsoft
 *
 */
final class StickyLoadBalancingStrategy implements LoadBalancingStrategy {
	private final CopyOnWriteArrayList<Host> hosts = new CopyOnWriteArrayList<Host>();
	private final AtomicInteger index = new AtomicInteger();

	@Override
	public void initialize(final Cluster cluster, final Collection<Host> hosts) {
		this.hosts.addAll(hosts);
		this.index.set(new Random().nextInt(Math.max(hosts.size(), 1)));
	}

	@Override
	public Iterator<Host> select(final RequestMessage msg) {
		final int startIndex = index.getAndIncrement();

		if (startIndex > Integer.MAX_VALUE - 10000)
			index.set(0);

		return new Iterator<Host>() {

			private int currentIndex = startIndex;

			@Override
			public boolean hasNext() {
				return hosts.size() > 0;
			}

			@Override
			public Host next() {
				int c = currentIndex++ % hosts.size();
				if (c < 0)
					c += hosts.size();
				return hosts.get(c);
			}
		};
	}

	@Override
	public void onAvailable(final Host host) {
		// Cosmos DB Gremlin-specific: Ignore this notification
	}

	@Override
	public void onUnavailable(final Host host) {
		// Cosmos DB Gremlin-specific: Ignore this notification
	}

	@Override
	public void onNew(final Host host) {
		this.hosts.addIfAbsent(host);
	}

	@Override
	public void onRemove(final Host host) {
		this.hosts.remove(host);
	}
}
```

To use sticky strategy please include the following snippet into your source code:

```
Cluster.Builder builder = Cluster.build();
//
// Configure builder as you normally would
//

// Configure special load balancing strategy for Azure that ignores host
// unavailability and continues to talk to the same host
builder.loadBalancingStrategy(new StickyLoadBalancingStrategy());

// Create a cluster and a client driver for a given cluster
Cluster cluster = builder.create();
Client client = cluster.connect();
```

## **Recommended Documents**  

[Azure Cosmos DB Gremlin server response headers and status codes](https://docs.microsoft.com/azure/cosmos-db/gremlin-headers)
<br>This article covers headers that Cosmos DB Gremlin server returns to the caller upon request execution. These headers are useful for troubleshooting request performance, building application that integrates natively with Cosmos DB service and simplifying customer support.  

[Apache TinkerPop Git Repository](https://github.com/apache/tinkerpop)


