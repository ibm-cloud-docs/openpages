---
copyright:
  years: 2025
lastupdated: "2025-07-28"

keywords: customize OpenPages, IBM OpenPages as a Service, OpenPages environment
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Customizing the hostname in the {{site.data.keyword.openpages_short}} URL
{: #customizing_hostname}

By default, instances have a system-generated hostname in the URL. You can change the hostname to create a more user-friendly URL. {: shortdesc}

You can also transfer a custom hostname from one instance to another.

[watsonx.governance]{: tag-blue} If you change the hostname, update the watsonx.governance integration to use the new hostname for {{site.data.keyword.openpages_short}}.

## Changing the hostname of an instance
{: #changing_hostname_instance}

To set a custom hostname, do the following steps:

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your {{site.data.keyword.openpages_short}} instance](/docs/openpages?topic=openpages-manage_op_instance).
2. Click **Environment**.
3. In the **Custom hostname** section, click the **Edit** icon.
4. Type a name, and then click **Save**. Wait a few minutes for the change to take effect.

   The last character in the hostname must not be a minus sign or a period. {:note: .note}

You can now launch {{site.data.keyword.openpages_short}} by using the **Custom hostname** URL or the **Fixed URL**.

## Transferring a hostname to another instance
{: #transferring_hostname_instance}

If you have multiple instances, you can transfer a custom hostname from one instance to another.

This feature enables you to provision a new instance without the need to give users a different URL.

To transfer a custom hostname to another instace, do the following steps:

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your {{site.data.keyword.openpages_short}} instance](/docs/openpages?topic=openpages-manage_op_instance).
2. Click **Environment**.

   The **Transfer hostname** section lists the custom hostnames of your other {{site.data.keyword.openpages_short}} instances.
3. Click a custom hostname, and then click **Transfer**.
4. Click **Transfer** to confirm the change.

When users go to the URL with the custom hostname, they are now using the instance that you selected in step 3.

## Providing users with the {{site.data.keyword.openpages_short}} URL
{: #provide_users_OP_url}

As an administrator, you can provide the {{site.data.keyword.openpages_short}} URL to your user community.

To get that URL to share with your users, do the following steps:

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [How to manage your IBM OpenPages instance](/docs/openpages?topic=openpages-manage_op_instance).
2. Choose one of the following options:
   - If you customized the hostname, click the **Copy** button of the **Custom hostname** URL.
   - If you didn't customize the hostname, click **Environment**. Under **Fixed URL**, click the **Copy** button.
