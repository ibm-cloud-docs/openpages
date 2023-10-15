---

copyright:
  years: 2023
lastupdated: "2023-10-15"

keywords: choosing a plan

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

# Choosing your plan
{: #openpages-choose-plan}

{{site.data.keyword.openpages_short}} is available in an Essentials plan or a Standard plan depending on your requirements.
{: shortdesc}

For information about {{site.data.keyword.openpages_short}} plan pricing, see the [catalog](https://cloud.ibm.com/catalog){: external}. Search for `{{site.data.keyword.openpages_short}}`, then click the {{site.data.keyword.openpages_short}} tile to go to the provisioning page.

## Essentials plan
{: #plan_essentials}

The Essentials plan is intended for users who want to try out {{site.data.keyword.openpages_short}} or build a proof-of-concept. Do not use the Essentials plan for production use. It offers shared access to a multi-tenant {{site.data.keyword.openpages_short}} cluster.

## Standard plan
{: #plan_standard}

The Standard plan is appropriate for production use. The Standard plan offers shared access to a multi-tenant {{site.data.keyword.openpages_short}} cluster that seamlessly autoscales as you increase the number of partitions you are using for your workload.

The architecture is highly available by default. The service is distributed across three availability zones, which means that the cluster is resilient to the failure of a single zone or any component within that zone.

## What is supported by the Essentials and Standard plans
{: #what_is_supported}

The following table summarizes what is supported by the plans:

| Category                         | Essentials Plan               | Standard Plan                 |
| -------------------------------- | ----------------------------- | ----------------------------- |
| Concurrent Users                 | 10                            | 200                           |
| Number of Solutions              | 1                             | 5                             |
| Ability to configure OpenPages   | Yes                           | Yes                           |
| Initial number of objects        | 10,000                        | 50,000                        |
| Number of objects per year       | 25,000                        | 100,000                       |
| Security Rules Limitations       | Intra-object only             | Intra-object only             |
| Number of permitted workflows    | 1 per object                  | 1 per object                  |
| Number of permitted Calculations | 2 per object                  | 10 per object                 |
| Number of permitted Operations   | 10 operations per calculation | 30 operations per calculation |
{: caption="Table 1. Plan comparison table" caption-side="bottom"}
