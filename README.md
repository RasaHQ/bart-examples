# bart-examples
Repo with example bots on different branches


1. Configure endpoints.yml
```yaml
tracing:
  type: otlp
  endpoint: localhost:4317
  insecure: true
  service_name: rasa

metrics:
  type: otlp
  endpoint: localhost:4317
  insecure: true
  service_name: rasa
```
2. run jaeger and prometheus:
```bash
docker compose up -d
```

4. run test
```bash
rasa test e2e e2e_tests/happy_paths/user_adds_contact_to_their_list.yml
```

5. check jaeger and prometheus dashboards
```yaml
http://localhost:16686/
http://localhost:9090/

```