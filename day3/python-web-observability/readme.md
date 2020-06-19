# KEYNOTE: Python->Web->Observability

We now live in a Cloud Native world where we build and deploy software very
differently from the previous generation. As companies began to build or migrate
to microservice architectures they often run into operational complexity and
struggle to efficiently monitor their environments. These challenges have
highlighted the need to observe systems differently and lead to the rise of
Observability.

---

Python web apps - Move to microservices
oBservability - Asking questions to answer unknowns
distributed tracing - the power of context and correlation
next steps - What does this mean for python and you?

---

## Observability

"Monitoring tells you whether the system works, observability lets you ask why its not working"
Baron Schwartz

3 pillars of observability:

- Logs
  - timestampped text with metadata
  - used for last mile analysis
- Metrics
  - time series data points w/metadata
  - often used to alert about a problem
- Traces
  - time based end-to-end request with RED (requests, errors, durations) metric and metadata
  - often used for problem isolation

Current state of python web:

- Logs
  - mostly logging
  - hard to use for debugging, mostly useful when added after the fact and redeployed
- metrics
  - some metrics
  - help perf tuning or raise alerts, but hardly help identify root causes
- errors
  - some error reporting
  - very specific to exceptions may not identify root cause and no way to identify impact

---

## Distributed Tracing

request id headers

W3C trace context <https://www.w3.org/TR/trace-context/>

Options for instrumentation:

<https://zipkin.io/>
<https://opencensus.io/>
<https://opentracing.io/>
<https://opentelemetry.io/>

Python OpenTelemetry Instrumentation:

`opentelemetry-<specific thing>` packages

Autoinstrumentation magic

## Next Steps

- Think about and plan for observability.
- Leverage FOSS & open standard instrumentation
- Be sure to enrich with metadata
- ensure you can ask any question with the data collected

<http://github.com/flands/pwc2020>
