---

copyright:
  years: 2025
lastupdated: "2025-04-28"

keywords: OpenPages release notes
subcollection: openpages
content-type: release-note

---
{{site.data.keyword.attribute-definition-list}}

# Release notes for {{site.data.keyword.openpages_short}}
{: #openpages-relnotes}

Use these release notes to learn about the latest updates to {{site.data.keyword.openpages_short}} that are grouped by date.
{: shortdesc}

## 28 April 2025
{: #openpages-apr2825}
{: release-note}

For AWS US East ( us-east-1 ) region

Bug fixes and security fixes
:   Bug fixes and security fixes were applied.

## 7 April 2025
{: #openpages-apr0725}
{: release-note}

For AWS US East ( us-east-1 ) and AWS Europe ( eu-central-1 ) regions

Using views to send input fields to custom models
:   In previous versions of OpenPages, an administrator could specify object fields to use as input to a custom model. Administrators can now configure a Task or Report View that contains the OpenPages fields that they want the model to process. Except for chart relationship fields, all object fields and relationship fields in the view are sent as input to the model. Users can access the insights from a model from the View AI insights button that the administrators can add to a view in View Designer.

Exporting data
:   You can export data from OpenPages® to be used outside of OpenPages in dashboarding and reporting applications, for Retrieval-Augmented Generation (RAG), and for other AI-based models. You must have the All Permissions/SOX/Administration/Data Export permission to run data exports.

Using @ mentions in object comments
:   In a comment on an object, users can now use @ mentions to tag other users. When they type @ followed by a few characters of the first name, last name, or username, a list of users is displayed. The user can then choose a name from the list.

Adding a Comment Activity panel to the dashboard
:   Users can add a panel on the dashboard to see the comments that they made and the comments in which they were mentioned.

Customizing email templates for comment notifications
:   Administrators can customize the template for emails that users receive when they are mentioned in a comment.

Reordering answers in questionnaire templates
:   Questionnaire template authors can now reorder the answers to a question.

Reflagging questions in questionnaire assessments
:   When a reviewer flags a question in a questionnaire and sends it back to the user to make changes, even if the reviewer accepts the new answer, the reviewer can later reflag the same question.

Using response actions in questionnaire templates to set an answer to an enumerated field
:   A questionnaire author can now use enumerated fields to set a field in the response actions of a questionnaire template.

Nested grids
:   An administrator can set up a nested grid for a Grid View or as a relationship field in a Task or Admin View. A nested grid displays the children of a specified object type and descendants of specified object types for each child. Each level of objects is indented to provide a visual representation of the relationships between the objects.

Ordering workflow actions
:   Administrators can now set the order of actions that a user sees when they click Action in a Task View. For example, an administrator can edit the properties of a stage to display the actions in the order of most often used to least often used.

Determining where fields are referenced
:   Administrators can now determine whether the references to a field are still needed by running a field reference analysis report. The report checks Views, Workflows, Profiles, Calculations, Security Rules, Filters, Dashboard Views, Field Dependencies, and Regulatory Event Rules for references to the field.

System migration - Exporting dependencies
:   You can export an item without exporting other items that it depends on. For example, you can export a view without its dependent object and field definitions. Also, unrelated content is no longer included in the export, which means that only items that are referenced by the exported item are included in the export.

System workflows
:   Only a scheduler job or another workflow can start a system workflow. When you use a system workflow, you ensure that the workflow runs consistently and at the right time, minimizing the risk of variations or errors.

Arabic (Saudi Arabia) and Arabic (United Arab Emirates) locales are available
:   Administrators can now add Arabic (Saudi Arabia) and Arabic (United Arab Emirates) as new locales. However, all numeric data such as currency, decimals, and time, use Western Arabic numerals, regardless of the regional preference.

Bug fixes and security fixes
:   Bug fixes and security fixes were applied.

## 28 February 2025
{: #openpages-feb2825}
{: release-note}

For AWS US East ( us-east-1 ) and AWS Europe ( eu-central-1 ) regions

Bug fixes and security fixes
:   Bug fixes and security fixes were applied.

## 27 January 2025
{: #openpages-jan2725}
{: release-note}

Bug fixes and security fixes
:   Bug fixes and security fixes were applied.

## 9 December 2024
{: #openpages-dec0924}
{: release-note}

Object commenting
:   Users can add their comments to objects if they are given permission by their administrator. For example, a user can add a comment on an Issue to ask a question, make an observation, or record their thoughts about the Issue.

Answers populated for questionnaire assessments
:   To populate the answers to a question with the values of a field, the questionnaire template authors associate the question with that field. An administrators adds the **Set questionnaire answers with related field value** operation to an action in the Questionnaire Assessment Workflow.

Delete objects by using a workflow
:   Administrators can define an end stage or an action in a workflow to delete objects.

Translation integration with watsonx.ai
:   When administrators use the watsonx.ai language translation service, they are able to define the prompt and the context for translation. With this feature, the large language model (LLM) can provide a translation that uses the industry-specific language of the Governance Risk and Compliance domain to provide more contextually appropriate translations.

Contextual information can be shared with IBM watsonx Assistant
:   Through the integration with IBM watsonx Assistant, OpenPages can share contextual information about the OpenPages user session. With this information, IBM watsonx Assistant knows the type of user that is logged on and where they are in the OpenPages UI. IBM watsonx Assistant can then use the OpenPages API to get more information, or perform actions on behalf of the user. For example, IBM watsonx Assistant can use generative AI to create an Action item for an issue in OpenPages.

Track email activity
:   Administrators can use a new system tracing option, **Email Notification**, to capture information about email activity that includes whether email messages are sent successfully.

Search for object types in the Primary menu
:   Users can now click the Primary menu and enter an object type in the **Search object type** box to find an object type.

Mexican Spanish locale available
:   Administrators can now add Mexican Spanish as a new locale.

Bug fixes and security fixes
:   Bug fixes and security fixes were applied.

## 7 November 2024
{: #openpages-nov0724}
{: release-note}

Region support
:   You can now deploy {{site.data.keyword.openpages_short}} in the AWS Europe (Frankfurt) region.

## 28 October 2024
{: #openpages-oct2824}
{: release-note}

Bug fixes and security fixes
:   Bug fixes and security fixes were applied.

## 23 September 2024
{: #openpages-sep2324}
{: release-note}

Warning message not displayed for non-entitled solutions on instances with sample data
:    If your instance of OpenPages as a Service is provisioned with sample data, you no longer see the warning that indicates your instance is using object types that are outside of the solutions that you are currently subscribed to.

Multiple custom tabs can be added to the OpenPages dashboard
:    The dashboard can now contain up to three custom tabs.

Ability to remove an added locale
:    You can now remove a locale that was previously added if you don't need it anymore.

Addition of stacked bar charts
:    You can now configure a stacked bar chart on the dashboard and the Task View Designer.

Addition of **Skip if it exists** functionality to questionnaire response actions that create a new object
:    If you don't want a response action to try re-creating a new object if an object by the same name already exists, select **Skip if it exists**.

Expressions supported when setting an object's field values based on a questionnaire respondent's answers
:    You can now enter an expression for the value of a field. For example, you can enter `[$TODAY$]` for the current date,`[$END_USER$]` for the name of the signed on user, or `[$System Fields:Description$]` to set the field to the value of the Description field of the object.

Session tracing
:    An administrator can set `/Applications/Common/Administration/Session Tracing` to enable tracing for a user's actions.

Capture of diagnostic data for database performance
:    You can use a new system tracing option to capture diagnostic data related to database performance.

Bug fixes and security fixes
:    Bug fixes and security fixes were applied.

## 26 August 2024
{: #openpages-aug2624}
{: release-note}

Bug fixes and security fixes
:    Bug fixes and security fixes were applied.

## 1 July 2024
{: #openpages-jul0124}
{: release-note}

Adding new locales
:    Administrators can now add new locales to provide translation support for languages other than the ones that OpenPages supports by default.

Adding images to rich text fields
:    For string fields that have a display type of Rich Text, users have a toolbar and commands for text formatting and word processing. This toolbar now contains a tool with which users can add an image to the field.

Exporting and importing dashboards by using the Environment Migration user interface
:    Prior to 9.0.0.3, dashboards could only be exported as part of a profile. Now you can export dashboards directly by using the Environment Migration UI.

Editing and deleting comments in questionnaires
:    Both respondents and reviewers can now edit or delete comments that they created in a questionnaire.

Make an answer exclusive for a multiple choice question
:    When editing a questionnaire template, a user can make an answer exclusive for a multiple choice question. When a respondent chooses an exclusive answer, they can't select another answer for the question. An example of an exclusive answer is "None of the above".

New endpoints available in the GRC REST API V2
:    There are new endpoints to automate FastMap import and validation, LogCollector processes, the retrieval of supported locales, and updating the values of configuration settings.

Additional security for your application
:    The default OpenPages Content Security Policy (CSP) has been improved to provide additional security for your application. CSP is an HTTP response header that browsers use to enhance the security of the document or web page. The CSP header allows you to restrict which resources, such as JavaScript, CSS, and images, can be loaded, and the URLs that they can be loaded from. The enhancements to security change the way OpenPages works. For more information, see [Content-Security-Policy (CSP) registry settings](https://www.ibm.com/docs/SSFUEU_9.0.0/op_grc_admin/c_adm_content-security-policy.html).

Bug fixes and security fixes
:    Bug fixes and security fixes were applied.

## 29 May 2024
{: #openpages-may2924}
{: release-note}

Bug fixes and security fixes
:    Bug fixes and security fixes were applied.

## 29 April 2024
{: #openpages-apr2924}
{: release-note}

Integration with watsonx.governance
:    You can now integrate watsonx.governance with {{site.data.keyword.openpages_short}}. To use this integration, the {{site.data.keyword.openpages_short}} Standard plan is required.

Amazon RDS for Db2
:    For new customers, {{site.data.keyword.openpages_short}} now uses Amazon RDS for Db2.

Bug fixes and security fixes
:    Bug fixes and security fixes were applied to fix errors and settings.

## 18 March 2024
{: #openpages-mar1824}
{: release-note}

Multiple reports in a single report view
:    Administrators can now define multiple report views for object types, giving users more options for viewing and sharing information.

New operation to associate objects in a workflow action
:    In a workflow, you can now add a new Associate objects operation on an action. This operation creates a relationship between the current object and other objects based on conditions that you specify.

Object creation based on questionnaire responses
:    On a questionnaire template, a questionnaire author can now create response actions to automatically create or copy an object and set field values on the object.

Configure a model to suggest relationships between objects
:    Administrators can now configure a model to suggest relationships between objects for the user. A relationship can be new or copied from an existing relationship.

Export and import questionnaire templates
:    You can now import and export questionnaire templates by using the Environment Migration user interface.

View low score questionnaires in Questionnaire Assessments
:    A questionnaire reviewer can now view questions with low scores by using the new View questions with low scores filter.

Translation services
:    {{site.data.keyword.openpages_full}} now supports NeuralSeek.

Support for future integration with watsonx.governance
:    {{site.data.keyword.openpages_full}} supports future integration with watsonx.governance (Standard Plan only)

Bug fixes and security fixes
:    Bug fixes and security fixes were applied to fix errors and settings.

## 6 February 2024
{: #openpages-feb0624}
{: release-note}

Bug fixes and security fixes
:    Bug fixes and security fixes were applied to fix errors and settings.

## 29 January 2024
{: #openpages-jan2924}
{: release-note}

Bug fixes and security fixes
:    Bug fixes and security fixes were applied to fix errors and settings.

## 4 December 2023
{: #openpages-dec0423}
{: release-note}

Bug fixes and security fixes
:    Bug fixes and security fixes were applied to fix errors and settings.

## 3 November 2023
{: #openpages-nov0323}
{: release-note}

Introducing {{site.data.keyword.openpages_short}}
:   {{site.data.keyword.openpages_full}} is an AI-driven, highly scalable governance, risk, and compliance (GRC) solution that runs on any cloud. Centralize siloed risk management functions within a single environment that is designed to help you identify, manage, monitor, and report on risk and regulatory compliance.
