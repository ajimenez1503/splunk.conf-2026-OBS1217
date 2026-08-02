# Create Alerts Input

## Configure Alerts input

- In the `Inputs` section, click `Create New Input` and select `Alerts Stream`.
- Fill in the form:
  - Name: enter a unique name.
  - ThousandEyes User: select your user.
  - Account Group: select your account group.
  - Alert Rules: select one or more alert rules to enable webhook notifications.
  - HEC Target: enter the HEC target for your Splunk instance. Example: `https://<host>:8088/services/collector/event`
  - HEC Token: select `ThousandEyesToken`.
  - Alerts Index: select `default`.
- Click `Add`.

!!! note "Automatic webhook configuration"
    The app creates a ThousandEyes webhook operation and a Splunk HEC connector, links them, and updates the selected alert rules to use the webhook for notifications.

![Alerts Stream input configuration](../img/thousandeyes_splunk_app/inputAlertsStream.png)

## View Alerts dashboard

- Trigger an alert for one of the selected alert rules.
- In the `Dashboards` section, select `Alerts`.

!!! note "Data may not be ready - Wait a few minutes"
    The alert must be triggered and sent to Splunk before it appears on the dashboard. This may take a few minutes.

![Alerts dashboard](../img/thousandeyes_splunk_app/dashboard_alerts.png)
