# Hands-on path after the guided UI

Start with the UI at Level 0. Explain each concept before using a command. Choose Practice lab, run a plan, inspect the exported evidence, and try the changed scenario. The assessment checks both scenarios and five questions.

## Python protocol examples

Activate `.venv`, then:

```bash
python -m scripts.http_demo
python -m scripts.http_demo --failure
# With the optional Collector running:
OTEL_EXPORTER_OTLP_TRACES_ENDPOINT=http://127.0.0.1:4318/v1/traces python -m scripts.http_demo
```

The UI runs the real OpenTelemetry Python SDK for logical checkout, payment, and database services in one process. It records actual spans, counters, histograms, correlated logs, propagated headers, and SDK timestamps. A separate runnable example adds real loopback HTTP boundaries and a real SQLite query; optional OTLP export reaches the official Collector.

## Complete local stack

Run `docker compose up --build -d`, then from the activated environment run:

```bash
python -m scripts.verify_stack
```

This verifies connected spans exported over real OTLP HTTP to the Collector. Container CI runs the same verifier with internal service URLs. Inspect `compose.yaml` for exact ports and configuration.

The default Collector prints telemetry using the debug exporter. Inspect `docker compose logs collector`. `examples/collector.yaml` is a loopback-only configuration for a local binary; `collector-container.yaml` binds the container interface with a loopback-only published host port. Run the official binary with `validate --config=examples/collector.yaml` before starting it. Its memory-limiter, attribute redaction, and batching are actual runtime components. A complete production backend and tail-sampling setup are additional exercises.

## Take the next step with evidence

Instrument your own small application, export to a storage backend, add service-to-service propagation, and compare trace evidence with application results. Measure sampling, queueing, dropped telemetry, memory, cardinality, privacy, and critical-path reasoning using a workload whose outcome you can verify.

UI service operations and N+1 calls are deliberately small local models, not production network or database benchmarks. Database restoration in the capstone is simulated. Head and parent-based sampling execute; tail sampling is taught but not implemented in the default SDK experiment. The Collector debug exporter prints telemetry; it is not a durable observability backend. YAML reference checks do not replace validation with the actual Collector binary.

Keep a record of what you directly observed, what the teaching model assumed, and what remains unknown. A troubleshooting conclusion should follow the same device or request through time and verify the relevant outcome.
