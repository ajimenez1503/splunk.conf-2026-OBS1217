# Service Map with Distributed Tracing

The Service Map integration connects ThousandEyes synthetic tests with Splunk Observability APM traces. When distributed tracing is enabled on a test, ThousandEyes injects trace headers into requests, the application continues the trace, and Splunk Observability receives the spans. ThousandEyes then queries Splunk APM to render the Service Map.

A pre-configured OpenTelemetry demo application is already running in the cloud and sending telemetry to a shared Splunk Observability instance. The application is already instrumented. You only need to configure the ThousandEyes side.

It is publicly accessible at [http://streaming-distributed-tracing-833293294.eu-central-1.elb.amazonaws.com/splunk/api/test](http://streaming-distributed-tracing-833293294.eu-central-1.elb.amazonaws.com/splunk/api/test).

## Workshop steps

1. [Create the Splunk APM Integration](basic/create_splunk_apm_integration.md)
2. [Create ThousandEyes HTTP Test](basic/create_thousandeyes_http_test.md)
3. [View the Service Map](basic/view_service_map.md)
