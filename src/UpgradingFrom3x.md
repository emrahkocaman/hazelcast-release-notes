
# Upgrading from 3.x


- **Introducing the `spring-aware` element:**
Before the release 3.5, Hazelcast uses `SpringManagedContext` to scan `SpringAware` annotations by default. This may cause some performance overhead for the users who do not use `SpringAware`.
This behavior has been changed with the release of Hazelcast 3.5. `SpringAware` annotations are disabled by default. By introducing the `spring-aware` element, now it is possible to enable it by adding the `<hz:spring-aware />` tag to the configuration. Please see the [Spring Integration section](#spring-integration).

- **Introducing new configuration options for WAN replication:**
Starting with the release 3.6, WAN replication related system properties, that are configured per node basis, can now be configured per target cluster.
Below 4 system properties are no more valid;

1. `hazelcast.enterprise.wanrep.batch.size`, please see the [WAN Replication Batch Size](#wan-replication-batch-size). 
2. `hazelcast.enterprise.wanrep.batchfrequency.seconds`, please see the [WAN Replication Batch Maximum Delay](#wan-replication-batch-maximum-delay).
3. `hazelcast.enterprise.wanrep.optimeout.millis`, please see the [WAN Replication Response Timeout](#wan-replication-response-timeout).
4. `hazelcast.enterprise.wanrep.queue.capacity`, please see the [WAN Replication Queue Capacity](#wan-replication-queue-capacity).






