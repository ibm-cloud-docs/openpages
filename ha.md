---

copyright:
  years: 2025
lastupdated: "2025-05-15"

keywords: high avalability, responsibilities

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Understanding high availability for {{site.data.keyword.openpages_full_notm}}
{: #ha}

[High availability](#x2284708){: term} (HA) is a core discipline in an IT infrastructure to keep your apps up and running, even after a partial or full site failure. The main purpose of high availability is to eliminate potential points of failures in an IT infrastructure.
{: shortdesc}

{{site.data.keyword.openpages_full}} is a highly available, multi-tenant, regional service. The service workload is distributed across multiple availability zones in a region, so single data center outage does not impact overall service availability. Data that is stored in {{site.data.keyword.openpages_short}} is replicated over the availability zones synchronously and is replicated to separate region asynchronously.

In addition to synchronous data replication across zones in one region, the underlying relational database takes full snapshot backup daily automatically and it is stored to regional S3 storage. The daily snapshot backup is kept for up to 35 days along with transaction logs, which is utilized by the service instance restore operation with point-in-time data.
For {{site.data.keyword.Bluemix_notm}}, IBM Db2 on Cloud Performance Plans provide high availability through a two-node High Availability Disaster Recovery (HADR) configuration. Each transaction is synchronously committed on both nodes, and in the event of a failure, the standby node automatically assumes write operations, minimizing downtime.

For more information on the restore operation, see [Backing up and restoring the database and configuration settings for IBM OpenPages](/docs/openpages?topic=openpages-backing_up_and_restoring&interface=ui).


## Responsibilities
{: #ha-responsibilities}

See [Shared responsibilities for IBM products.](/docs/overview?topic=overview-shared-responsibilities) for details on responsibility ownership between {{site.data.keyword.IBM_notm}} and the customer when using {{site.data.keyword.openpages_short}}.

## What level of availability does {{site.data.keyword.cloud_notm}} offer?
{: #ha-service}

The level of availability that you set up for your cluster impacts your coverage under the {{site.data.keyword.cloud_notm}} high availability service level agreement terms.

Service level objectives (SLOs) describe the design points that the {{site.data.keyword.cloud_notm}} services are engineered to meet. {{site.data.keyword.openpages_short}} is designed to achieve the following availability target.

| Availability target | Target Value   |
|---|---|
|  Availability % | 99.9  |
{: caption="SLO for {{site.data.keyword.openpages_short}}" caption-side="bottom"}

The SLO is not a warranty and {{site.data.keyword.IBM_notm}} will not issue credits for failure to meet an objective. Refer to the SLAs for commitments and credits that are issued for failure to meet any committed SLAs. For a summary of all SLOs, see [{{site.data.keyword.cloud_notm}} service level objectives](/docs/overview?topic=overview-slas).
