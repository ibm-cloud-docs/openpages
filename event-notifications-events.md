---

copyright:
  years: 2026
lastupdated: "2026-02-20"

keywords: Enabling event notifications OpenPages, IBM Cloud,

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}



# Enabling event notifications for {{site.data.keyword.openpages_short}}
{: #event-notifications-events}



As an administrator of {{site.data.keyword.openpages_short}}, you might want to send notifications of events in {{site.data.keyword.openpages_short}} to other users, or human destinations, by using email, SMS, or other supported delivery channels. Additionally, you might want to send these notifications of events to other applications to build logic by using event-driven programming that uses webhooks, for example. This is made possible by the integration between {{site.data.keyword.openpages_short}} and {{site.data.keyword.en_full}}.
{: shortdesc}

To send information to {{site.data.keyword.en_short}}, you must connect your {{site.data.keyword.openpages_short}} instance to {{site.data.keyword.en_short}}. For more information about working with {{site.data.keyword.en_short}}, see [Getting started with {{site.data.keyword.en_short}}](/docs/event-notifications?topic=event-notifications-getting-started).

## How events are collected and sent by {{site.data.keyword.openpages_short}}
{: #event-notifications-how}

When an event of interest takes place in your {{site.data.keyword.openpages_short}} instance, {{site.data.keyword.openpages_short}} communicates with a connected {{site.data.keyword.en_short}} instance to forward a notification to a [supported destination](/docs/event-notifications?topic=event-notifications-getting-started#en-decide-event-destination).

Currently, {{site.data.keyword.openpages_short}} supports only email destinations.

{{site.data.keyword.openpages_short}} uses a simplified event model where all alert notifications are sent using a single event type (`com.ibm.cloud.openpages.event`). The differentiation between different types of notifications happens at the content level within the event payload, which follows the CloudEvents v1.0 specification.



## Events for {{site.data.keyword.openpages_short}}
{: #event-notifications-list}

The following table lists the {{site.data.keyword.openpages_short}} events. All events are under the `com.ibm.cloud.openpages.event` subtype.



| Event type                                  | Description |
|------------------------------------------|---------|
| `com.ibm.cloud.openpages.event`           | Generic {{site.data.keyword.openpages_short}} event for all alert notifications |
{: caption="Actions that generate event notifications" caption-side="bottom"}

## Event payload format
{: #event-notifications-payload}

{{site.data.keyword.openpages_short}} sends notifications following the CloudEvents v1.0 specification. Each event contains structured information about the notification, including recipient details and the complete email content.

### Payload structure
{: #event-notifications-payload-structure}

The following example shows the structure of an event payload sent from {{site.data.keyword.openpages_short}} to {{site.data.keyword.en_short}}:

```json
{
  "specversion": "1.0",
  "id": "crn:v1:staging:public:openpages:global:a/2ac0a95fe03740b6977da3d5333898f3:eb51158d-405e-404c-a1c7-79bf2122dc9c::1967579992",
  "source": "openpages",
  "type": "com.ibm.cloud.openpages.event",
  "ibmensourceid": "crn:v1:staging:public:openpages:global:a/2ac0a95fe03740b6977da3d5333898f3:eb51158d-405e-404c-a1c7-79bf2122dc9c::",
  "ibmendefaultshort": "<truncated body>",
  "ibmendefaultlong": "<truncated body>",
  "message_subject": "<email subject>",
  "message_html_body": "<!DOCTYPE HTML> <html> <head></head> <body style=\"font-family: ibm-plex-sans,HelveticaNeue,Helvetica,Arial,sans-serif; font-size: 14px;\"> <h1 style=\"font-size: 20px; font-weight: 300; padding: 22px 24px;\"><span style=\"font-weight: 600\">IBM OpenPages</span></h1> <hr style=\"margin: 0; border-bottom: 2px solid #0f62fe\" /> <div style=\"padding: 8px 24px 32px; background-color: #f3f3f3;\"> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\">Workflow name:</h2> <p style=\"margin: 0\">Requirement Evaluation</p> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\">Object type:</h2> <p style=\"margin: 0\">Requirement Evaluation</p> </div> <div style=\"padding: 8px 24px 160px;\"> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\"> Number of object (evaluated):</h2> <p style=\"margin: 0\">13</p> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\"> Number of workflow started successfully:</h2> <p style=\"margin: 0\">0</p> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\"> Number of workflow skipped (applicability, locked, already in workflow):</h2> <p style=\"margin: 0\">13</p> <div style=\"display:none\"> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\"> Number of workflow failed to start:</h2> <p style=\"margin: 0\">0</p> <h2 style=\"font-size: 14px; font-weight: 600; margin: 24px 0 8px;\"> Failed workflows (first 100 objects):</h2> <ul>  </ul> </div> </div> <hr style=\"margin: 0; border-bottom: 1px solid #767676\" /> <div style=\"padding: 32px 24px;\">This email was automatically generated by IBM OpenPages.</div> </body> </html>",
  "ibmenmailto": ["<recipient1>", "<recipient2>", ...]
}
```
{: codeblock}

### Payload properties
{: #event-notifications-payload-properties}

The following table describes the properties in the event notification payload:

| Property          | Type   | Description                                                   |
|-------------------|--------|---------------------------------------------------------------|
| `specversion`       | String | CloudEvents specification version                             |
| `id`                | String | Unique event identifier: `<CRN><jobId.hashCode()>`               |
| `source`            | String | Event source identifier (always "openpages")                  |
| `type`              | String | Event type (always "com.ibm.cloud.openpages.event")           |
| `ibmensourceid`     | String | IBM Event Notifications source ID (CRN of OpenPages instance) |
| `ibmendefaultshort` | String | Short notification message (truncated email body)             |
| `ibmendefaultlong`  | String | Long notification message (truncated email body)              |
| `message_subject`   | String | Email subject line                                            |
| `message_html_body` | String | Complete HTML-formatted email body                            |
| `ibmenmailto`       | Array  | JSON array of recipient email addresses                       |
{: caption="Event notification payload properties" caption-side="bottom"}

### Data size limits
{: #event-notifications-payload-limits}

The following table shows the maximum size limits for event payload fields:

| Field             | Maximum Size                           | Truncation Applied              |
|-------------------|----------------------------------------|---------------------------------|
| `ibmendefaultshort` | 1000 characters                        | Yes - truncated from email body |
| `ibmendefaultlong`  | 3000 characters                        | Yes - truncated from email body |
| `message_subject`   | No explicit limit                      | No                              |
| `message_html_body` | No explicit limit                      | No                              |
| `ibmenmailto`       | No explicit limit                      | No                              |
| `specversion`       | Fixed: "1.0"                           | N/A                             |
| `source`            | Fixed: "openpages"                     | N/A                             |
| `type`              | Fixed: "com.ibm.cloud.openpages.event" | N/A                             |
{: caption="Data size limits for event payload fields" caption-side="bottom"}

## Enabling notifications
{: #event-notifications-enable}

Events that are generated by an instance of the {{site.data.keyword.openpages_short}} service can be forwarded to an {{site.data.keyword.en_short}} service instance that is available in the same account. You can configure only one {{site.data.keyword.openpages_short}} instance to one {{site.data.keyword.en_short}} service instance. However, a single {{site.data.keyword.en_short}} service instance can have many {{site.data.keyword.openpages_short}} instances pointing to it.

The following table shows the {{site.data.keyword.openpages_short}} service instance regions and the {{site.data.keyword.en_short}} service regions that they can forward events to:

| {{site.data.keyword.openpages_short}} service instance region | Supported {{site.data.keyword.en_short}} service region |
| --- | --- |
| AWS US East ( us-east-1 ) |  {{site.data.keyword.Bluemix_notm}} Dallas ( us-south ) |
| AWS Europe ( eu-central-1 ) | {{site.data.keyword.Bluemix_notm}} Frankfurt ( eu-de ) |
| {{site.data.keyword.Bluemix_notm}} Sydney (au-syd) | {{site.data.keyword.Bluemix_notm}} Sydney (au-syd) |
{: caption="{{site.data.keyword.openpages_short}} service instance regions and their corresponding {{site.data.keyword.en_short}} service regions" caption-side="bottom"}

### Adding an {{site.data.keyword.en_short}} service instance
{: #event-notifications-add-service}

Before you can enable notifications for {{site.data.keyword.openpages_short}}, add an [{{site.data.keyword.en_short}} service instance](/catalog/services/event-notifications){: external} to the same account as your {{site.data.keyword.openpages_short}} instance.

1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your {{site.data.keyword.openpages_short}} instance](/docs/openpages?topic=openpages-manage_op_instance).
2. Click **Settings**.
3. In the {{site.data.keyword.en_short}} section, and click **Connect**.
4. Expand **Before you begin**.
5. Click **Create new instance**.
6. On the Event Notifications Pricing page, select a plan, click the checkbox to agree to the license agreement, and then click **Create**.

### Connecting to {{site.data.keyword.en_short}}
{: #event-notifications-enable-ui}
{: ui}

Connect {{site.data.keyword.openpages_short}} to the  {{site.data.keyword.en_short}} service instance by using **Settings > Event Notifications** section in the {{site.data.keyword.openpages_short}} UI to connect the services.



1. Go to the UI where you manage your {{site.data.keyword.openpages_short}} instance. For more information, see [Managing your {{site.data.keyword.openpages_short}} instance](/docs/openpages?topic=openpages-manage_op_instance).
2. In the {{site.data.keyword.openpages_short}} navigation, click **Settings**.
3. In the {{site.data.keyword.en_short}} section, click **Connect**.
4. In the **Event Notification instances** section, click **Event Notifications service instance** and select the {{site.data.keyword.en_short}} that you created.
5. To confirm the connection, click **Save**.
   The Event Notifications section shows the connection between the {{site.data.keyword.openpages_short}} instance and the Event Notifications instance.
6. You can verify that a topic and subscription are created for your {{site.data.keyword.openpages_short}} instance in the **Event Notification** settings by clicking on the **Review** link.

Your {{site.data.keyword.openpages_short}} instance is ready to send notifications.

## Delivering notifications to select destinations
{: #event-notifications-destinations}

After you enable notifications for {{site.data.keyword.openpages_short}}, create topics and subscriptions in {{site.data.keyword.en_short}} so that alerts can be forwarded and delivered.

{{site.data.keyword.openpages_short}} notifications are in HTML format and are intended for the email delivery channel.



### Email notifications
{: #event-notifications-email}

You can use the [{{site.data.keyword.cloud_notm}} email service](/docs/event-notifications?topic=event-notifications-en-destinations-email) as a delivery channel for {{site.data.keyword.openpages_short}} event notifications. [Create an {{site.data.keyword.en_short}} subscription](/docs/event-notifications?topic=event-notifications-en-create-en-subscription) between an existing topic and the {{site.data.keyword.cloud_notm}} email service to forward your alerts to various recipients by email. Recipients are automatically set based on the activity within {{site.data.keyword.openpages_short}} that caused the notification to be created.

These emails originate from `no-reply@cloud.ibm.com` or `event-notifications@cloud.ibm.com`, but you can specify your own reply-to address.



The email content is provided in HTML format within the `message_html_body` field of the event payload. For more information about the payload structure, see [Event payload format](#event-notifications-payload).
{: tip}
