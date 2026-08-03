# Visualize ThousandEyes Page Load HAR as a Trace in Splunk Observability Cloud

In this step you'll explore your ThousandEyes page-load data as an APM trace in Observability Cloud, drilling into each span of the page load.

- Log in to [Splunk Observability Cloud](../getting_started/login_splunk_observability.md)
- From the landing page, navigate to `APM` -> `Trace Analyzer`

![Trace view](../img/splunk_observability/o11y_apm_nav.png)

- Filter by `Services` and enter the service you configured for your test
    - For example, `www.cisco.com` or `*cisco*`

![Search traces](../img/splunk_observability/o11y_trace_filter_svc.png)

- Click `Add Filters` and create a filter: `thousandeyes.test.name = <your-test-name>` 
    - For example, `thousandeyes.test.name = ofushtei-1217-page-load-cisco`

![Search by ThousandEyes test name](../img/splunk_observability/o11y_trace_filter_test.png)

- Click on the trace to view its details

![Trace details](../img/splunk_observability/o11y_trace_view.png)

- Each span represents a step in the page load and contains:
    - Span information: ID, URL, method, duration, and status code

    ![span request details](../img/splunk_observability/o11y_trace_details_1.png)
    
    - ThousandEyes metadata: account, test, agent, and stream

    ![span thousandeyes details](../img/splunk_observability/o11y_trace_details_2.png)
