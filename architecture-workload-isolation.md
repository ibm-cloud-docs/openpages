---

copyright:
  years: 2020, 2023
lastupdated: "2023-03-08"

keywords:

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}
<!--
_Name your file `architecture-workload-isolation.md` and include it in the **How to** nav group in the **Enhancing security** topic group in your `toc.yaml` file. See https://test.cloud.ibm.com/docs/writing?topic=writing-security-content-guidance_

_Make sure that you use the following title for your topic._-->

# Learning about {{site.data.keyword.openpages_short}} architecture and workload isolation
{: #compute-isolation}

<!-- The title of your H1 should be Learning about _servicename_ architecture and workload isolation, where _service-name_ is the non-trademarked short version keyref, but the first occurrence in your topic is the trademarked version. Include your service name as a search keyword at the top of your Markdown file. See the example keywords above. -->

_The short description should be a single, concise paragraph that contains one or two sentences and no more than 50 words. Summarize your offering's architecture and support for isolating one tenants' workload from another._

Review the following sample architecture for  {{site.data.keyword.openpages_short}}, and learn more about different isolation levels so that you can choose the solution that best meets the requirements of the workloads that you want to run in the cloud.
{: shortdesc}

## {{site.data.keyword.openpages_short}} architecture
{: #architecture}

Provide an architectural overview diagram identifying what runs within the IBM Service Account and what runs in the customer's account.

CW: IBM Cloud docs team says this is a good example to follow: https://cloud.ibm.com/docs/secrets-manager?topic=secrets-manager-compute-isolation

## {{site.data.keyword.openpages_short}} workload isolation
{: #workload-isolation}

Document how customer workloads are isolated from each other by plan. Do customer workloads run within the customer account?  Are customer workloads isolated within Kubernetes namespaces? Do customer workloads run on dedicated compute?
