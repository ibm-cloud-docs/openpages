---

copyright:
  years: 2025
lastupdated: "2025-05-12"

keywords:

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

# Learning about {{site.data.keyword.openpages_short}} as a Service architecture and workload isolation
{: #compute-isolation}

{{site.data.keyword.openpages_short}} as a Service is a multi-tenant service with dedicated resources per tenant. To learn more, review the following architecture diagram to see how {{site.data.keyword.openpages_short}} can meet the requirements of the sensitive workloads that you want to run in the cloud.
{: shortdesc}

## {{site.data.keyword.openpages_short}} as a Service architecture
{: #architecture}

The following image shows the main components of {{site.data.keyword.openpages_short}} as a Service.

![Tenant isolation architecture](images/op_saas_tenant_isolation.png "Tenant isolation architecture"){: caption="Main components of OpenPages as a Service - AWS" caption-side="bottom"}


![Tenant isolation architecture](images/op_saas_tenant_isolation_ibmcloud.png "Tenant isolation architecture"){: caption="Main components of OpenPages as a Service - {{site.data.keyword.Bluemix_notm}}" caption-side="bottom"}


- A service instance of {{site.data.keyword.openpages_short}} uses a dedicated RDBMS service instance and a dedicated document storage folder at the data layer.

- Application pods on the {{site.data.keyword.redhat_openshift_full}} cluster are allocated in a dedicated fashion for {{site.data.keyword.openpages_short}} service instances. Tenant network is isolated by the {{site.data.keyword.redhat_openshift_full}} namespace with network policy.
- The {{site.data.keyword.openpages_short}} service assigns a dedicated URL for each service instance for accessing the application by using the web UI, API, or CLI. The network edge nodes and load balancers are shared across tenants and the requests are dispatched to the application per the service instance URL.

## {{site.data.keyword.openpages_short}} as a Service workload isolation
{: #workload-isolation}

The {{site.data.keyword.openpages_short}} service assigns a dedicated URL, dedicated application pods, a dedicated RDMS service, and dedicated S3 document storage folder for each instance. The tenant workload is isolated all the way from the network layer, to the application layer, to the data layer.
