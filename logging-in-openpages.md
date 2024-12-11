---

copyright:
  years: 2024
lastupdated: "2024-12-11"

keywords: logging

subcollection:  openpages

---

{{site.data.keyword.attribute-definition-list}}



# Logging for {{site.data.keyword.openpages_short}}
{: #logging}

{{site.data.keyword.cloud_notm}} services, such as {{site.data.keyword.openpages_short}}, generate platform logs that you can use to investigate abnormal activity and critical actions in your account, and troubleshoot problems.
{: shortdesc}

You can use {{site.data.keyword.logs_routing_full_notm}}, a platform service, to route platform logs in your account to a destination of your choice by configuring a tenant that defines where platform logs are sent. For more information, see [About Logs Routing](/docs/logs-router?topic=logs-router-about).

You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on platform logs that are generated in your account and routed by {{site.data.keyword.logs_routing_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.



As of 28 March 2024, the {{site.data.keyword.la_full_notm}} service is deprecated and will no longer be supported as of 30 March 2025. Customers will need to migrate to {{site.data.keyword.logs_full_notm}} before 30 March 2025. During the migration period, customers can use {{site.data.keyword.la_full_notm}} along with {{site.data.keyword.logs_full_notm}}. Logging is the same for both services. For information about migrating from {{site.data.keyword.la_full_notm}} to {{site.data.keyword.logs_full_notm}} and running the services in parallel, see [migration planning](/docs/cloud-logs?topic=cloud-logs-migration-intro).
{: important}

## Locations where logs are sent by {{site.data.keyword.logs_routing_full_notm}}
{: #lr-locations}



The following table shows the {{site.data.keyword.openpages_short}} service instance regions that generate platform logs and the {{site.data.keyword.logs_routing_full_notm}} locations that they can send them to:
| {{site.data.keyword.openpages_short}} service instance region | {{site.data.keyword.logs_routing_full_notm}} location |
| --- | --- |
| AWS US East ( us-east-1 ) |  IBM Cloud Dallas ( us-south ) |
| AWS Europe ( eu-central-1 ) | IBM Cloud Frankfurt ( eu-de ) |
{: caption="{{site.data.keyword.openpages_short}} service instance regions and their corresponding {{site.data.keyword.logs_routing_full_notm}} locations" caption-side="bottom"}

## Platform logs that are generated
{: #log-platform}



{{site.data.keyword.openpages_short}} generates platform logs for the error, warning, and critical severity types. 



## Enabling logging
{: #log-enable}









Create {{site.data.keyword.logs_full_notm}} and configure routing by setting the target between source location to target instance.

## Viewing logs
{: #log-viewing}



To view {{site.data.keyword.openpages_short}} logs, go to the [Logging instance page](https://cloud.ibm.com/observability/logging){: external} and click the {{site.data.keyword.logs_full_notm}} instance.

### Launching {{site.data.keyword.logs_full_notm}} from the Observability page
{: #log-launch-standalone}



For more information about launching the {{site.data.keyword.logs_full_notm}} UI, see [Launching the UI in the {{site.data.keyword.logs_full_notm}} documentation](/docs/cloud-logs?topic=cloud-logs-instance-launch).

## Fields by log type
{: #log-fields}



For information about fields included in every platform log, see [Fields that are included in platform logs](/docs/logs-router?topic=logs-router-about-platform-logs#about-platform-logs-2).





{{site.data.keyword.openpages_short}} logs include the following fields.

| Field             | Type       | Description             |
|-------------------|------------|-------------------------|
| `logSourceCRN`    | Required   | Defines the account and flow log instance where the log is published. |
| `saveServiceCopy` | Required   | Defines whether IBM saves a copy of the record for operational purposes. |
| `message`         | Required   | Description of the log that is generated. |
| `messageID`       | Required   | ID of the log that is generated. |
{: caption="Log record fields" caption-side="bottom"}

{{site.data.keyword.openpages_short}} sends audit events as platform logs. For more information, see [Auditing events for IBM OpenPages](/docs/openpages?topic=openpages-at_events).

## Analyzing {{site.data.keyword.openpages_short}} logs
{: #cloud-logs}



In the {{site.data.keyword.logs_full_notm}} dashboard, users can filter based on **Application**, **Subsystem**, and **Severity** to find logs specific to an instance. Users can also create a custom dashboard, view logs, or write a query to search for a log data.

They can also create **alerts** in the {{site.data.keyword.logs_full_notm}}.
