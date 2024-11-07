---

copyright:
  years: 2024
lastupdated: "2024-11-07"
keywords: OpenPages as a Service, business continuity

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}



# Understanding business continuity and disaster recovery for {{site.data.keyword.openpages_short}}
{: #bc-dr}

[Disaster recovery](#x2113280){: term} involves a set of policies, tools, and procedures for returning a system, an application, or an entire data center to full operation after a catastrophic interruption. It includes procedures for copying and storing an installed system's essential data in a secure location, and for recovering that data to restore normalcy of operation.
{: shortdesc}

## Responsibilities
{: #bc-dr-responsibilities}

To find out more about responsibility ownership for using {{site.data.keyword.cloud}} products between {{site.data.keyword.IBM_notm}} and customer see [Shared responsibilities for {{site.data.keyword.cloud_notm}} products](/docs/overview?topic=overview-shared-responsibilities).

## Disaster recovery strategy
{: #bc-dr-strategy}

{{site.data.keyword.cloud_notm}} has [business continuity](#x3026801){: term} plans in place to provide for the recovery of services within hours if a disaster occurs. You are responsible for your data backup and associated recovery of your content.

{{site.data.keyword.openpages_short}} provides mechanisms to protect your data and restore service functions. Business continuity plans are in place to achieve targeted [recovery point objective](#x3429911){: term} (RPO) and [recovery time objective](#x3167918){: term} (RTO) for the service. The following table outlines the targets for {{site.data.keyword.openpages_short}}.

| Disaster recovery objective | Target Value   |
|---|---|
|  RPO | Up to 24 hours  |
|  RTO | Up to 72 hours  |
{: caption="RPO and RTO for {{site.data.keyword.openpages_short}}" caption-side="bottom"}

The service is restored to another region based on the following table. The application URL domain is updated in the event of a restore. When the service is restored at the target region, the new application URL is available in the console.

If you customized the hostname, the URL uses the updated region, along with the custom hostname.

| Primary region of the service | Target region to restore the service   |
|---|---|
|  AWS US East (Northern Virginia) | AWS US East (Ohio)  |
|  AWS Europe (Frankfurt) | AWS Europe (London) / eu-west-2  |
{: caption="Regions for {{site.data.keyword.openpages_short}}" caption-side="bottom"}
