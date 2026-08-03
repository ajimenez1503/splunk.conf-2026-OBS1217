# Integrate Splunk ITSI with ThousandEyes

This guide explains how to integrate Cisco ThousandEyes with Splunk IT Service Intelligence (ITSI).
The integration enables you to ingest test data, send alert notifications, and visualize Splunk episodes directly in ThousandEyes.

## Update the Index Used by the Content Pack

If your data stream does not use the default `thousandeyes` index, you need to update the content pack's search macro to match your selected index. For this workshop, we used the `thousandeyes_data` index.

- From the Splunk Enterprise main menu, select `Settings` -> `Advanced Search`
- Select `Search Macros`
- In the **App** drop-down menu, select `Cisco ThousandEyes (DA-ITSI-CP-thousandeyes)`
- Select `itsi_cp_thousandeyes_index`
    - By default, the macro definition is set to `index="thousandeyes"`
- In the **Definition** field, change the index value to the index used by the Cisco ThousandEyes App for Splunk
    - During this workshop, we used `thousandeyes_data` index
- Click `Save`
