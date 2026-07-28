# Visualize ThousandEyes Page Load HAR as a trace in Splunk Observability Cloud 

## Navigate to the APM page

- Log in to the [Splunk Observability Cloud](../getting_started/login_splunk_observability.md)
- From the landing page, navigate to `APM` -> `Trace Analyzer`

![Trace view](../img/splunk_observability/o11y_apm_nav.png)

- Filter by `Services` and enter the service you configured your test for
    - For example, `www.cisco.com` or `*cisco*`

![Search traces](../img/splunk_observability/o11y_trace_filter_svc.png)

- Click Add Filters and create a filter `thousandeyes.test.name = <your-test-name>` 
    - For example, `thousandeyes.test.name = ofushtei-1217-page-load-cisco`

![Search by ThousandEyes test name](../img/splunk_observability/o11y_trace_filter_test.png)

- Click on the trace to view details

![Trace details](../img/splunk_observability/o11y_trace_view.png)

- Each span will be a step in the page load and contains:
    - Information about the span: ID, URL, method, duration, and status code

        ![span request details](../img/splunk_observability/o11y_trace_details_1.png)
    
    - ThousandEyes identification: account, test, agent, stream

        ![span thousandeyes details](../img/splunk_observability/o11y_trace_details_2.png)
