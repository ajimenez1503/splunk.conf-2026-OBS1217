# Stream ThousandEyes Test Data to Splunk ITSI

In this step you'll install the content pack, which turns ThousandEyes metrics (latency, loss, jitter, DNS) into ready-made **ITSI services and KPIs**.

## Prerequisites

By default, this integration expects you to ingest ThousandEyes Metrics via the Cisco ThousandEyes App.

If you haven't completed this yet, please follow the [workshop guide](../thousandeyes_splunk_app/test_metrics_stream_input.md) or the [official documentation](https://docs.thousandeyes.com/product-documentation/integration-guides/custom-built-integrations/splunk-app/itsi#stream-thousandeyes-test-data-to-splunk-itsi)

## Install and Configure the Content Pack

To install and configure the Content Pack for Cisco ThousandEyes, follow these steps:

- Go to `ITSI` -> `Configuration` -> `Data Integrations` -> `Content Library`
- Select `Cisco ThousandEyes` from the list
- Click `Proceed`
- Add all objects (both `New` and `Already installed`)
- Click `Import as enabled`
- Click `Activate all saved searches`
- Optionally, add a prefix to help with the filtering, for example: `<your-unique-id>-obs1217-`
- Click `Backfill service KPIs`
- Click `Install selected`, then `Install` in the confirmation dialog

![ThousandEyes Content Pack configuration](../img/itsi/itsi_te_pack_config.png)

## Validate installation

To validate your installation:

- Go to `Service Analyzer` -> `Default Analyzer`
- Filter services by the prefix you specified during configuration
- If you don't see any results, try extending the time range

Services reporting health scores means the data path is working end to end.

![ITSI Service Analyzer validation](../img/itsi/itsi_te_validation.png)

