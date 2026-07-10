# Service Map with Distributed Tracing

The Service Map integration connects ThousandEyes synthetic tests with Splunk Observability APM traces. When distributed tracing is enabled on a test, ThousandEyes injects trace headers into requests, the application continues the trace, and Splunk Observability receives the spans. ThousandEyes then queries Splunk APM to render the Service Map.

For this 30-minute workshop, a pre-configured OpenTelemetry demo application is already running and sending telemetry to a shared Splunk Observability instance. You only need to configure the ThousandEyes side.

**Start here:** [Getting Started](basic/getting_started.md)

## Workshop steps

1. [Create the Splunk APM Integration](basic/create_splunk_apm_integration.md)
2. [Create ThousandEyes HTTP Test](basic/create_thousandeyes_http_test.md)
3. [View the Service Map](basic/view_service_map.md)
