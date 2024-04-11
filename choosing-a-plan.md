---

copyright:
  years: 2024
lastupdated: "2024-04-11"

keywords: choosing a plan, pricing plans

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

# How does {{site.data.keyword.openpages_short}} calculate pricing?
{: #openpages-choose-plan}

Customers are charged for {{site.data.keyword.openpages_short}} on a monthly basis. The charge is based on the maximum amount of consumption over the course of the month.
{: shortdesc}

Solutions are charged at the account level. If the same solution is active in multiple environments, customers are charged only once for that solution.

The following table shows some examples of monthly charges.

| Scenario                                                                                                                                                                                       | Charge                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| A customer provisions a single instance on day 1.\nThe customer provisions a second instance on day 15.\nThe customer deprovisions the second instance on day 25.                                                  | The charge for that month is for the two instances.             |
| A customer has an instance that is being used as a production environment with ORM active.\nThe customer also has a second instance that is being used as a non-production environment with ORM active. | The customer is charged only once for the use of that solution. |
| A customer has an instance that is being used as a production environment with ORM active.\nThe  customer has a second instance that is being used as a non-production environment with ORM and RCM active.     | The customer is charged for the two solutions: ORM and RCM.     |
{: caption="Table 1. Examples of charges." caption-side="bottom"}

For more information about {{site.data.keyword.openpages_short}} pricing, see the [catalog](https://cloud.ibm.com/catalog){: external}. Search for `{{site.data.keyword.openpages_short}}`, then click the {{site.data.keyword.openpages_short}} tile to go to the provisioning page.

## Plan types
{: #plan-types}

You can choose a plan based on your requirements. The service offers two pricing plans.

### Essentials
{: #plan_essentials}

The Essentials plan is ideal for small organizations or departments within a larger organization who are looking to get started with a GRC solution. It can also be used as a non-production environment.

### Standard
{: #plan_standard}

The Standard plan is ideal for small to medium-sized organizations or departments in larger organization who are looking for expanded use of GRC solutions.

[watsonx.governance]{: tag-blue} To integrate with watsonx.governance, the Standard plan is required.

## What is supported by the Essentials and Standard plans
{: #what_is_supported}

The following table summarizes what is supported by each plan. The values in the table are maximums.

| Category                                     | Essentials plan               | Standard plan                 |
| -------------------------------------------- | ----------------------------- | ----------------------------- |
| Concurrent users                             | 10                            | 200                           |
| Number of solutions                          | 1                             | 5                             |
| Ability to configure OpenPages               | Yes                           | Yes                           |
| Initial number of objects                    | 10,000                        | 50,000                        |
| Number of objects per year                   | 25,000                        | 100,000                       |
| Security rules limitations                   | Intra-object only             | Intra-object only             |
| Number of permitted workflows                | 1 per object                  | 1 per object                  |
| Number of permitted calculations             | 2 per object                  | 10 per object                 |
| Number of permitted operations               | 10 operations per calculation | 30 operations per calculation |
| Supports integration with watsonx.governance | No                            | Yes                           |
| Custom objects                               | Not permitted                 | Not permitted                 |
{: caption="Table 1: What is supported by each plan." caption-side="bottom"}
