# ThousandEyes - Splunk Integrations Workshop



Welcome to **"ThousandEyes & Splunk Integration workshop"**

During this session you will learn about: 

- [**Visualizing the service map using distributed tracing in ThousandEyes**](service_map/basic/getting_started.md)
- [**Streaming ThousandEyes data to Splunk Observability Cloud**](getting_started/login_splunk_observability.md)
- [**Streaming ThousandEyes data to Splunk Cloud Platform or Splunk Enterprise**](splunk_core/login_splunk_cloud_enterprise.md)
- [**Exploring the capabilities of the Cisco ThousandEyes App for Splunk**](thousandeyes_splunk_app/getting_started.md)

![workflow](img/workflow_diagram.png)

## Prerequisites

To prepare for this Workshop:

- Have accounts for:
    - [ThousandEyes](https://www.thousandeyes.com) — a workshop account is provided in [**ThousandEyes**](getting_started/thousandeyes.md)
    - [Splunk Observability Cloud](https://www.splunk.com/en_us/products/observability-cloud.html) — a workshop account is provided in [**Log In to Splunk Observability Cloud**](getting_started/login_splunk_observability.md)
    - [Splunk Cloud Platform](https://www.splunk.com/en_us/products/splunk-cloud-platform.html) or [Splunk Enterprise](https://www.splunk.com/en_us/products/splunk-enterprise.html) (free trial is not valid due to the [issue](https://ideas.splunk.com/ideas/PLECID-I-816))
        - Version requirements: 9.4 or later.
- Permissions and roles:
    - ThousandEyes: 
        - View/Edit streaming integrations
        - View/Edit tests
    - Splunk Observability Cloud: role `power` or `admin` (to create access tokens and dashboards).
    - Splunk Cloud Platform / Splunk Enterprise: role `admin` or `sc_admin`.
- All workshop steps are completed in the ThousandEyes and Splunk web UIs — no API tools are required.
- Go through [**ThousandEyes**](getting_started/thousandeyes.md) and [**Log In to Splunk Observability Cloud**](getting_started/login_splunk_observability.md) before starting the different sections of the Workshop

## Other integrations

- [Stream ThousandEyes alerts to Splunk Cloud Platform or Splunk Enterprise](https://docs.thousandeyes.com/product-documentation/integration-guides/custom-webhook-examples/splunk-alert-notifs)
