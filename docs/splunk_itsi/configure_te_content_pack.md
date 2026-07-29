# Configure the Content Pack for Cisco ThousandEyes

To the Content Pack for Cisco ThousandEyes, do the following:
- Navigate to `ITSI` -> `Configuration` -> `Data Integratiions` -> `Content Library`
- Select `Cisco ThousandEyes` from the list
- Follow the steps from the official ThousandEyes documentation: [Splunk ITSI Integration # Install the Content Pack for Cisco ThousandEyes](https://docs.thousandeyes.com/product-documentation/integration-guides/custom-built-integrations/splunk-app/itsi#install-the-content-pack-for-cisco-thousandeyes)
    - Click `Proceed`
    - Add all objects (both `New` and `Already installed`)
    - Click `Import as enabled`
    - Click `Activate all saved searches`
    - Click `Backfill service KPIs`
    - Click `Install selected`
    - In the confirmation dialog, click `Install`
- To validate the installation, go to `Service Analyzer` -> `Default Analyzer`
    - Filter services by the prefix you specified during the configuration
    - If you don't see results, try extending the time range