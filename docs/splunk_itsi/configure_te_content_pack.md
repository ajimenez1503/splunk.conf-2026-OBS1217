# Stream ThousandEyes Test Data to Splunk ITSI

## Prerequisites

By default, this integration expects you to ingest ThousandEyes Metrics via the Cisco ThousandEyes App.

If you haven't complete this yet, please follow the [workshop guide](../thousandeyes_splunk_app/test_metrics_stream_input.md) or the [official documentation](https://docs.thousandeyes.com/product-documentation/integration-guides/custom-built-integrations/splunk-app/itsi#stream-thousandeyes-test-data-to-splunk-itsi)

## Install and Configure the Content Pack

To install and configure the Content Pack for Cisco ThousandEyes, follow these steps:

- Navigate to `ITSI` -> `Configuration` -> `Data Integrations` -> `Content Library`
- Select `Cisco ThousandEyes` from the list
- Follow the steps from the official ThousandEyes documentation: [Splunk ITSI Integration # Install the Content Pack for Cisco ThousandEyes](https://docs.thousandeyes.com/product-documentation/integration-guides/custom-built-integrations/splunk-app/itsi#install-the-content-pack-for-cisco-thousandeyes)
    - Click `Proceed`
    - Add all objects (both `New` and `Already installed`)
    - Click `Import as enabled`
    - Click `Activate all saved searches`
    - Click `Backfill service KPIs`
    - Click `Install selected`
    - In the confirmation dialog, click `Install`

![ThousandEyes Content Pack configuration](../img/itsi/itsi_te_pack_config.png)

## Validate installation

To validate your installation:

- Go to `Service Analyzer` -> `Default Analyzer`
- Filter services by the prefix you specified during the configuration
- If you don't see any results, try extending the time range

![ITSI Service Analyzer validation](../img/itsi/itsi_te_validation.png)

