---
copyright:
  years: 2024
lastupdated: "2024-09-23"

keywords: openpages maintenance, availability of operations

subcollection: openpages

content-type: learn

---

{{site.data.keyword.attribute-definition-list}}

# Maintenance windows
{: #maintenance-windows}

To ensure that {{site.data.keyword.openpages_full}} environments are up to date with the latest software and security patches, routine maintenance windows are required.

The schedule is as follows:
| Region             |  Schedule                |
| ------------------ | ------------------------ |
| AWS US East (Northern Virginia) | Sunday 11 PM - Monday 7 AM EST (Monday 4 AM - 12 PM UTC) |
{: caption="Table 1. Schedule of maintenance windows by region" caption-side="bottom"}

The maintenance window might be extended in some circumstances, for example due to public holidays.
{: note}

During the maintenance window, the {{site.data.keyword.openpages_full}} system is available for use, except for background or asynchronous operations such as the following operations:

- FastMap import
- Import configuration
- Export configuration
- Reporting schema operations
- Object Reset operations
- Large volume copy, move, and associate operations
- Start workflow operations for applicable objects from the administrative page
- Start calculation operations for applicable objects from the administrative page
- ObjectManager `load`, `dump`, `batch`, and `validate` operations from the {{site.data.keyword.cloud}} command-line plugin
- Scheduler jobs
- Questionnaire program launch operations

The underlying infrastructure, relational database system, and application server pod are restarted with patches and updates during the maintenance window.

For information about the overall status of the service, see the [Status Overview](https://cloud.ibm.com/status) page.
