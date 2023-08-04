---

copyright:
  years: 2020, 2023

lastupdated: "2023-03-08"

keywords:

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

<!--Name your file `service-endpoints.md` with the title Using service endpoints to privately connect to _servicename_. When nav titles are available you can use Using service endpoints as your title for the left nav entry while retaining the longer title as your H1 in the topic to ensure helpful search results.
IMPORTANT:
* If your service supports only service endpoints, include it in the **How to** nav group in the **Enhancing security** topic group in your `toc.yaml` file.
* If your service supports both service endpoints and VPE for VPC, then refer to the guidance about placement in a nested topic group within the Enhancing security topic group: https://test.cloud.ibm.com/docs/writing?topic=writing-security-content-guidance-->

# Managing an allowed IP list for {{site.data.keyword.openpages_short}}
{: #service-endpoints}

To ensure that you have enhanced control and security over your data when you use {{site.data.keyword.openpages_short}}, you have the option of specifying the IP addresses that are allowed to connect to your {{site.data.keyword.openpages_short}} service instance.
{: shortdesc}

By default, all IP addresses can be used to log in to {{site.data.keyword.openpages_short}} and access the API.

_Required: Document any customer data that goes over public routes even with the IBM Cloud service endpoints feature enabled using a connection over private routes. For example, if your service sends customer data to a data-service using a public route or sends customer logs using public routes to LogDNA that should be documented._

## Before you begin
{: #prereq-service-ip}

You have an {{site.data.keyword.openpages_short}} instance.

_any other prerequisities?_

## Setting up allowed IP addresses
{: #add-service-ip}

1. In your web browser, go to the **Resource List**.
2. Under **AI / Machine Learning**, click the **Name** of the instance.
3. On the {{site.data.keyword.openpages_short}} Overview tab, go to the **Administrative Actions** section.
4. In the **IP Allowlisting** table, click **New**.
5. Enter an IP address (IPv4, IPv6, or CIDR) and a description, then click **Save**.

     The IP addresses listed in the **IP Allowlisting** table are the only ones from which clients can access {{site.data.keyword.openpages_short}}.

## Removing IP addresses from the allow-list
{: #endpoint-disable}

_anything to note here?_
