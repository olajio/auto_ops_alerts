When configuring alerts using **AutoOps in Elastic Cloud**, it's crucial to prioritize alerts that directly impact **cluster health, performance, data ingestion, and availability**. Here’s a breakdown of the **most important alerts** you should consider:

---

### 🔴 **Critical Cluster Health & Availability Alerts**

These are non-negotiables—alerting on them ensures your cluster doesn’t go into a degraded or unusable state.

* **Cluster Health status is RED**

  * Indicates one or more primary shards are unavailable.
* **Cluster Health status is YELLOW for prolonged period**

  * Indicates unassigned replica shards—useful for warning before RED.
* **Cluster unavailable**

  * Detects full outages (no nodes responding).

---

### 📉 **Ingestion Failures & Pipeline Issues**

Without data ingestion, Elastic loses relevance fast.

* **Indexing failure rate**

  * Detects issues with bulk ingest or log pipelines.
* **Beats/Logstash pipeline failure**

  * Alerts when ingestion pipelines stop or error out.
* **Logstash node offline**

  * Ensures your pipeline is active and ingesting.

---

### 🧠 **Resource Exhaustion / Performance Bottlenecks**

Preempt infrastructure issues like high latency, slow queries, or memory pressure.

* **High JVM heap usage (over 85%)**

  * Signals memory pressure. Can lead to GC pauses or crashes.
* **Disk usage over threshold (e.g. 80–85%)**

  * Prevents “read-only index” scenarios or total failure if disk fills up.
* **CPU usage consistently high**

  * Indicates node overload, misconfigured queries, or heavy ingestion.
* **Queue size growing (search or write thread pools)**

  * Early signal of bottlenecks in handling requests or writes.

---

### 🔐 **Security / Access Alerts**

For secure clusters with sensitive data, monitor access control and threats.

* **Audit log entries with failed logins**
* **Excessive login attempts or unusual access patterns**
* **Users accessing sensitive indices (e.g. `.security`, `.kibana`, etc.)**

---

### 📦 **Snapshot and Backup Alerts**

Backups are only useful if they work.

* **Snapshot failure**

  * Alerts on failed scheduled snapshots (critical for disaster recovery).
* **Repository unavailable**

  * Detects unreachable snapshot storage (e.g., S3).

---

### 🧪 **Watchers / Custom Rules**

If you have custom watchers or rule-based alerts:

* **Watcher execution errors**
* **Long watch execution time**
* **Notification delivery failures (e.g., Slack/email not going through)**

---

### ✅ Best Practices

* **Set thresholds based on trends** from monitoring dashboards (e.g., alerts when disk usage grows 5% daily).
* **Add runbooks or links in alert messages** to speed up response.
* **Test each alert configuration** using test data or thresholds.

---

Would you like me to generate an **AutoOps JSON/YAML alert template** for these common alerts, or walk through how to configure one via the Kibana UI?
