# Test Plan Template

## Test Name


## Goal


## System Under Test


## Environment

- Application version:
- Database version:
- Infrastructure:
- Source hash:

## Scenario


## Load Profile

- Tenants:
- Users:
- Target RPS:
- Duration:
- Read/write ratio:
- Background jobs:

## Acceptance Criteria

- p95 latency:
- p99 latency:
- error rate:
- queue recovery:
- correctness:

## Stop Conditions

- sustained 5xx:
- deadlock:
- data corruption:
- DB pool exhaustion:
- severe p99 degradation:

## Observability

- Metrics:
- Logs:
- Traces:
- Dashboards:
