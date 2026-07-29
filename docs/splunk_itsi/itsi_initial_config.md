# Integrate Splunk ITSI with ThousandEyes

This guide explains how to integrate Cisco ThousandEyes with Splunk IT Service Intelligence.
The integration enables you to ingest test data, send alert notifications, and visualize Splunk episodes directly in ThousandEyes.

## Prerequisites

To integrate ITSI and ThousandEyes, you need the following:
- Splunk ITSI version 4.20.x or later
- Cisco ThousandEyes App for Splunk verstion 0.1.0 or later
- Splunk App for Content Packs version 2.3.0 or later, including 2 Content Packs:
    - ITSI Monitoring and Alerting
    - Cisco ThousandEyes 

Luckily for you, everything is already installed

## Update the Index Used by the Content Pack

If your data stream does not use the thousandeyes index, you need update the content pack's search macro to match your selected index. And during our workshop, we used `thousandeyes_data` index.

- From the Splunk Enterprise main menu, select `Settings`, then `Advanced Search`
- Select `Search Macros`
- In the App drop-down menu, select `Cisco ThousandEyes (DA-ITSI-CP-thousandeyes)`
- Select `itsi_cp_thousandeyes_index`
    - By default, the macro definition is set to `index="thousandeyes"`
- In the Definition field, change the index value to the index used by the Cisco ThousandEyes App for Splunk
    - During this workshop, we used `thousandeyes_data` index
- Click `Save`
