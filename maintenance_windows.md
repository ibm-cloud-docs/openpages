---
copyright:
  years: 2024
lastupdated: "2024-03-15"

keywords: openpages maintenance, availability of operations

subcollection: openpages

content-type: learn

---

{{site.data.keyword.attribute-definition-list}}

# Maintenance windows
{: #maintenance-windows}

To ensure the {{site.data.keyword.openpages_full}} environments are up to date with the latest software and security patches, routine maintenance windows are required. 

The schedule is as follows:

| Region                          | Schedule                                               |
| ------------------------------- | ------------------------------------------------------ |
| AWS US East (Northern Virginia) | Sunday 11PM - Monday 7AM EST ( Monday 4AM - 12PM UTC ) |
{: caption="Table 1. Schedule of maintenance windows by region" caption-side="bottom"}

During the maintenance window, the {{site.data.keyword.openpages_full}} system is available for use,  except for background or asynchronous operations such as the following operations:

- FastMap import
- Import configuration
- Export configuration
- Reporting schema operations
- Object Reset operations
- Large volume copy, move, and associate operations
- Start workflow operations for applicable objects from the administrative page
- Start calculation operations for applicable objects from the administrative page
- Object Manager load, dump, and validate operations from the {{site.data.keyword.cloud}} command line plugin
- Scheduler jobs
- Questionnaire program launch operations

The underlying infrastructure, relational database system, and application server pod are restarted with patches and updates during the maintenance window.
