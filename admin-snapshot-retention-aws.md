---
copyright:
  years: 2026
lastupdated: "2026-06-26"

keywords: snapshot retention, monthly snapshots, backup retention, compliance

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Configuring snapshot retention for {{site.data.keyword.openpages_short}}
{: #snapshot-retention}

You can configure monthly snapshot retention policies for your instances to meet compliance and auditing requirements. Monthly snapshots are automatically created and retained according to your configured policy.
{: shortdesc}

Snapshot retention is available for all plan types.

This feature is applicable to {{site.data.keyword.openpages_short}} on AWS Marketplace.
{: note}

## About monthly snapshot retention
{: #about-snapshot-retention}

Monthly snapshots are automatically created on the 1st of each month at 2:00 AM UTC. You can choose to retain these snapshots for 1, 3, 7, or 10 years.

### Storage lifecycle
{: #storage-lifecycle}

Monthly snapshots follow this automated lifecycle:

- **AWS Backup service**: Snapshots are stored in AWS Backup vault with warm storage for the first 90 days, then automatically moved to cold storage
- **S3 Storage**: Additional backup copies are maintained in S3 with Standard storage for 30 days, then transitioned to Glacier storage
- **Retention**: Data is retained according to your configured policy (1, 3, 7, or 10 years)
- **Deletion**: Data is permanently purged after the retention period expires

## Configuring snapshot retention
{: #configure-snapshot-retention}

To configure monthly snapshot retention for your instance, do the following steps:

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your IBM OpenPages instance](/docs/openpages?topic=openpages-manage_op_instance).

2. Click **Environment**.

3. Scroll down to the **Snapshot retention** section.

4. Click the **Retention period** dropdown menu.

5. Select your desired retention period:

| Retention Period | Use Case                                    |
| ------------------| ---------------------------------------------|
| 1 year           | Development and testing environments        |
| 3 years          | Standard compliance requirements            |
| 7 years          | Extended compliance                         |
| 10 years         | Maximum retention for regulatory compliance |
{: caption="Available snapshot retention periods" caption-side="bottom"}

6. Click **Save**. Wait for the confirmation message indicating that the snapshot retention has been successfully updated.

The new retention period is displayed in the **Snapshot retention** section.

Changes to the retention policy apply to future snapshots. Existing snapshots continue to follow their original retention schedule.
{: important}

## Configuring different retention policies for multiple instances
{: #multiple-instances-retention}

If you have multiple instances in your dedicated cluster (for example, development, production, and QA), you can configure different retention policies for each instance.

To configure different retention policies, do the following steps:

1. Navigate to the UI where you manage each {{site.data.keyword.openpages_short}} instance separately.

2. Follow the steps in [Configuring snapshot retention](#configure-snapshot-retention) for each instance.

3. Configure the appropriate retention period based on each instance's requirements:
   - **Production instances**: Typically require longer retention (7 or 10 years) for compliance
   - **QA or staging instances**: May use shorter retention (1 or 3 years)
   - **Development instances**: Often use the minimum retention (1 year)
