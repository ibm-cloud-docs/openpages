---

copyright:
  years: 2023
lastupdated: "2023-10-18"

keywords: high avalability, responsibilities

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}
<!--Name your file `ha.md` and include it in the **Reference** nav group in your `toc.yaml` file.-->

# Understanding high availability for {{site.data.keyword.openpages_short}}
{: #ha}

[High availability](#x2284708){: term} (HA) is a core discipline in an IT infrastructure to keep your apps up and running, even after a partial or full site failure. The main purpose of high availability is to eliminate potential points of failures in an IT infrastructure.
{: shortdesc}

## Responsibilities
{: #ha-responsibilities}

<!-- If there is specific responsibility documentation for the product , comment the next paragraph-->
<!-- To find out more about responsibility ownership for using {{site.data.keyword.cloud}} products between {{site.data.keyword.IBM_notm}} and the customer, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} products](/docs/overview?topic=overview-shared-responsibilities).-->

<!-- If there is specific responsibility documentation available for the product, provide a linked reference on the following paragraph or elaborate on the current document-->

See [Shared responsibilities for IBM products.](/docs/overview?topic=overview-shared-responsibilities) for details on responsibility ownership between {{site.data.keyword.IBM_notm}} and the customer when using {{site.data.keyword.openpages_short}}.

{{site.data.keyword.openpages_long}} is a highly available, multi-tenant, regional service. The service workload is distributed across multiple availability zones in a region, so single data center outage does not impact overall service availability. Data that is stored in {{site.data.keyword.openpages_short}} is replicated over the availability zones synchronously and is replicated to separate region asynchronously.

## What level of availability does {{site.data.keyword.cloud_notm}} offer?
{: #ha-service}

The level of availability that you set up for your cluster impacts your coverage under the {{site.data.keyword.cloud_notm}} high availability service level agreement terms.

Service level objectives (SLOs) describe the design points that the {{site.data.keyword.cloud_notm}} services are engineered to meet. {{site.data.keyword.openpages_short}} is designed to achieve the following availability target.

| Availability target | Target Value   |
|---|---|
|  Availability % | 99.99  |
{: caption="Table 1. SLO for {{site.data.keyword.openpages_short}}" caption-side="bottom"}

The SLO is not a warranty and {{site.data.keyword.IBM_notm}} will not issue credits for failure to meet an objective. Refer to the SLAs for commitments and credits that are issued for failure to meet any committed SLAs. For a summary of all SLOs, see [{{site.data.keyword.cloud_notm}} service level objectives](/docs/overview?topic=overview-slo).

