---
copyright:
  years: 2024
lastupdated: "2024-01-03"

keywords: backing up OpenPages, restoring OpenPages
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Backing up and restoring the database and configuration settings for {{site.data.keyword.openpages_short}}
{: #backing_up_and_restoring}

Incremental backups run automatically when there is a change to the database or the
configuration settings. These backups are retained for 35 days.
{: shortdesc}

A restore creates a new {{site.data.keyword.openpages_short}} instance that is a copy of the backed-up instance.

To restore a backup, do the following steps:
1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your IBM OpenPages instance](/docs/openpages?topic=openpages-manage_op_instance).
2. Click **Environment**.
3. Click **Backup and restore**.
4. Enter a **Service name** for the new {{site.data.keyword.openpages_short}} instance.
5. Choose one of the following options:
   - Select **Latest restorable time** if you want the most recent backup to be restored.
   - Select **Custom date and time** if you want to choose a particular backup to be restored.

      - Click **Choose a date** and select a date.
      - Click **Choose a time** and enter a time.

**Important:**

- The backup you choose must have been created at an earlier date and time than the latest backup.
- Ensure that you choose a date and time at least one hour after your instance was provisioned, or your instance might fail to restore.

When the restore is complete, the new instance is available for you to access.

[watsonx.governance]{: tag-blue} When you restore {{site.data.keyword.openpages_short}}, the integration with watsonx.governance is not restored. You need to re-enable the integration.
