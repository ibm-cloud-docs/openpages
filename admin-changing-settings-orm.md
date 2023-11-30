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

1. Download the following package and extract the zip file: [ORMAssessmentMethodUpdate.zip](https://github.ibm.com/OpenPages/backlog/files/1248551/ORMAssessmentMethodUpdate.zip) 
2. Set java_home in `<OP_HOME>/Module/loaderdata/AssessmentMethodUpdate/post_install_update_ORM_assessment_settings.sh|.bat.`
3. Run the following script:

    Linux:
    ```console
        cd <OP_HOME>/Module/loaderdata/AssessmentMethodUpdate 
        ./post_install_update_ORM_assessment_settings.sh <likelihood_count>
                                <impact_count>
                                <assessment_method_type>                     
    ```

    Windows:
    ```console
        cd <OP_HOME>\Module\loaderdata\AssessmentMethodUpdate 
        post_install_update_ORM_assessment_settings.bat <likelihood_count>
                                <impact_count>
                                <assessment_method_type>
                                
    ```

    The script parameters are as follows: 
    - `<likelihood_count>` is a value between 1 and 10.
    - `<impact_count>` is a value between 1 and 10.
    - `<assessment_method_type>` is qualitative or quantitative.

    The script modifies the following loader file with the settings that you passed to the script: `<OP_HOME>/Module/loaderdataORM/AssessmentMethodUpdate_PostInstall/ORM-assessment-settings-op-config.xml`

4. Import the loader file into OpenPages. You can use **ObjectManager** or **Import Configuration**.

    **ObjectManager:**

    Run the following command for Linux, Windows, and MacOS: 
    ```console 
        ibmcloud openpages objectmanager load ORM/AssessmentMethodUpdate_PostInstall ORM-assessment-settings
    ```
    
    For more information, see [Load command example](https://www.ibm.com/docs/en/openpages/9.0.0?topic=commands-load-command-example). To learn more about the `ibmcloud CLI plugin`, see [{{site.data.keyword.openpages_short}} CLI (ibmcloud openpages)](/docs/openpages?topic=openpages-openpages_CLI&interface=ui). 

    **Import Configuration:**

    Click the **Administration menu** > **System Migration** > **Import Configuration**. Validate the `<OP_HOME>/Module/loaderdataORM/AssessmentMethodUpdate_PostInstall/ORM-assessment-settings-op-config.xml` file and then import it.
    For more information, see [Importing configuration items to the target environment](https://www.ibm.com/docs/en/openpages/9.0.0?topic=environments-importing-configuration-items-target-environment).

5. Verify the following changes:
   - Log in to OpenPages.
   - Click the **Administration menu** > **Solution Configuration** > **Calculations**.
   - Verify that the calculation for the assessment type that you chose is enabled.
    For example, if you changed the assessment type to Qualitative, verify that **Qualitative Risk Rating** is enabled and **Quantitative Risk Rating** is disabled.

<!--6. Update the deploy.properties files with the new values for ORM.
    - Open the `<op_installer>/src/deployment/<deployment_name>/deploy.properties` file in a text editor.
    - Update the following properties:

    ```text
        module_assessment_method =
        module_likelihood_count =
        module_impact_count =
    ```
--> 


