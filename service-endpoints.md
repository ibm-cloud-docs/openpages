---

copyright:
  years: 2024
lastupdated: "2024-09-06"

keywords: Managing IP addresses OpenPages, IP addresses, IBM Cloud

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}



# Managing IP addresses for {{site.data.keyword.openpages_short}}
{: #service-endpoints}

To ensure that you have enhanced control and security over your data when you use {{site.data.keyword.openpages_short}}, you have the option of specifying the IP addresses that are allowed to connect to your {{site.data.keyword.openpages_short}} service instance.
{: shortdesc}

By default, all IP addresses can be used to log in to {{site.data.keyword.openpages_short}} and access the API.



## Before you begin
{: #prereq-service-ip}

Ensure that you have an {{site.data.keyword.openpages_short}} instance.

If you need to create an {{site.data.keyword.openpages_short}} instance, see [Provisioning your IBM OpenPages as a Service environment](/docs/openpages?topic=openpages-provisioning_environment&interface=api)


## Setting up allowed IP addresses
{: #add-service-ip}

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your {{site.data.keyword.openpages_short}} instance](/docs/openpages?topic=openpages-manage_op_instance).
2. Click the **Settings** tab.
3. In the **IP Allowlisting** table, click **New**.
4. Enter an IP address (IPv4, IPv6, or CIDR) and a description, then click **Save**.

     The IP addresses listed in the **IP Allowlisting** table are the only ones from which clients can access {{site.data.keyword.openpages_short}}.

## Removing IP addresses from the allow-list
{: #endpoint-disable}

You can remove IP addresses from the **IP Allowlisting** table by following the next steps:

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your {{site.data.keyword.openpages_short}} instance](/docs/openpages?topic=openpages-manage_op_instance).
2. On the **{{site.data.keyword.openpages_short}} Overview** tab, go to the **Administrative Actions** section.
3. In the **IP Allowlisting** table, click the **Delete** icon in the **Actions** column.

    The IP address is removed from the **IP Allowlisting** table.
