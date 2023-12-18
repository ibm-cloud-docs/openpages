---
copyright:
  years: 2023
lastupdated: "2023-11-30"

keywords: operational risk management, ORM, risk assessments
subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Changing the settings for assessments in {{site.data.keyword.openpages_short}} Operational Risk Management
{: #set_orc}

If you haven't created any objects yet, you can change the settings for risk assessments. These settings are used by IBM OpenPages® Operational Risk Management.
{: shortdesc}

When you provision {{site.data.keyword.openpages_full_notm}} environment, the ORM module's assessment method is configured as qualitative with 10 total likelihood count and 10 total impact count.

You can change these settings later by running a script. The script updates a loader file, which you then import into OpenPages to re-configure ORM.

If you've already created objects, you can run the script but any existing objects are not updated. You might need to do some manual remediation. The script is designed for fresh installations of ORM.{: note}

1. Download the **ORMAssessmentMethodUpdate.zip** package from Fix Central.
2. Create a new directory called ORM.
3. Extract the zip file into the ORM directory.
4. Set `java_home` in `AssessmentMethodUpdate/post_install_update_ORM_assessment_settings.sh|.bat`
5. Run the following command:

    Linux:
    ```console
        cd AssessmentMethodUpdate./post_install_update_ORM_assessment_settings.sh <likelihood_count> <impact_count> <assessment_method_type>
    ```

    Windows:
    ```console
        cd AssessmentMethodUpdatepost_install_update_ORM_assessment_settings.bat <likelihood_count> <impact_count> <assessment_method_type>
    ```

    The script parameters are as follows:
    - `<likelihood_count>` is a value between 1 and 10.
    - `<impact_count>` is a value between 1 and 10.
    - `<assessment_method_type>` is `qualitative` or `quantitative`.

    The script modifies the following loader file with the settings that you passed to the script: `AssessmentMethodUpdate_PostInstall/ORM-assessment-settings-op-config.xml`

6. Import the loader file into {{site.data.keyword.openpages_short}}. You can use **ObjectManager** or **Import Configuration**.

    **ObjectManager:**

    Run the following command for Linux, Windows, and MacOS:
    ```console
        ibmcloud openpages objectmanager load ORM/AssessmentMethodUpdate_PostInstall ORM-assessment-settings
    ```

   To learn more about the `ibmcloud CLI plugin`, see [{{site.data.keyword.openpages_short}} CLI (ibmcloud openpages)](/docs/openpages/openpages_cli.md).

    **Import Configuration:**

    Click **Administration menu** > **System Migration** > **Import Configuration**. Validate the `AssessmentMethodUpdate_PostInstall/ORM-assessment-settings-op-config.xml` file and then import it.
    For more information, see [Importing configuration items to the target environment](https://www.ibm.com/docs/en/openpages/9.0.0?topic=environments-importing-configuration-items-target-environment).

6. Verify the changes:
   - Log in to {{site.data.keyword.openpages_short}}.
   - Click **Administration menu** > **Solution Configuration** > **Calculations**.
   - Verify that the calculation for the assessment type that you chose is enabled.
    For example, if you changed the assessment type to Qualitative, verify that **Qualitative Risk Rating** is enabled and **Quantitative Risk Rating** is disabled.
