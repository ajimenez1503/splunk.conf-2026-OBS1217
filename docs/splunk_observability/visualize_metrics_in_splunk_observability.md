# Visualize ThousandEyes Metrics in Splunk Observability Cloud


## Navigate to the Network monitoring dashboard

**ThousandEyes Network monitoring** dashboard is already created in the Splunk Observability Cloud instance.

- Log in to the [Splunk Observability Cloud](../getting_started/login_splunk_observability.md)
- From the landing page, navigate to `Dashboards`
- In `Custom dashboard groups`, click on `ThousandEyes Network monitoring` and select `Application` from the dropdown

![dashboards](../img/splunk_observability/o11y_te_dash_nav.png)

## Visualize your test data

Other participants share the same Splunk Observability environment, so make sure you are viewing metrics for **your** ThousandEyes test only.

- Once the dashboard is loaded, enter the test name in the `ThousandEyes Test` field
- Use **ThousandEyes test name** you chose when creating your Page Load test

If you don't see data immediately, just wait a few minutes. Telemetry needs to be generated and sent to Splunk.

**Application dashboard**

![Dashboard Application](../img/splunk_observability/o11y_te_dash_app.png)

**Network dashboards**

![Dashboard Network](../img/splunk_observability/o11y_te_dash_network.png)
